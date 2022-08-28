Створює пару нерозрізнених сокетів і зберігає їх у масиві

-   [« socket\_create\_listen](function.socket-create-listen.html)
    
-   [socket\_create »](function.socket-create.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Створює пару нерозрізнених сокетів і зберігає їх у масиві
    

# socketcreatepair

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketcreatepair - Створює пару нерозрізнених сокетів і зберігає їх у масиві

### Опис

```methodsynopsis
socket_create_pair(    int $domain,    int $type,    int $protocol,    array &$pair): bool
```

**socketcreatepair()** створює два сполучених і нерозрізняються сокети, і зберігає їх у масиві `pair`. Ця функція зазвичай використовується IPC (міжпроцесної взаємодії).

### Список параметрів

`domain`

Параметр `domain` визначає сімейство протоколів, яке використовуватиметься сокетом. Перегляньте їх повний список в описі функції [socket\_create()](function.socket-create.html)

`type`

Параметр `type` вказує тип комунікації, яка використовуватиметься сокетом. Перегляньте їх повний список в описі функції [socket\_create()](function.socket-create.html)

`protocol`

Параметр `protocol` встановлює певний протокол у зазначеному сімействі протоколів `domain`, який використовуватиметься у зв'язку з отриманими сокетами. Відповідне значення може бути отримано на ім'я за допомогою функції [getprotobyname()](function.getprotobyname.html). Якщо потрібний протокол TCP чи UDP, то відповідні константи **`SOL_TCP`** і **`SOL_UDP`** також можуть бути використані.

Дивіться повний список протоколів, що підтримуються в описі функції [socket\_create()](function.socket-create.html)

`pair`

Посилання на масив, в який буде вставлено два екземпляри [Socket](class.socket.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                  |
|--------|---------------------------------------------------------------------------------------------------------------------------|
|        | `pair` є посиланням на масив екземплярів [Socket](class.socket.html); раніше був посиланням на масив ресурсів (resource). |

### Приклади

**Приклад #1 Приклад використання **socketcreatepair()****

```php
<?php
$sockets = array();

/* На Windows нам нужно использовать AF_INET */
$domain = (strtoupper(substr(PHP_OS, 0, 3)) == 'WIN' ? AF_INET : AF_UNIX);

/* Создаём пару сокетов */
if (socket_create_pair($domain, SOCK_STREAM, 0, $sockets) === false) {
    echo "Не получилось выполнить socket_create_pair. Причина: ".socket_strerror(socket_last_error());
}
/* Отправляем и получаем данные */
if (socket_write($sockets[0], "ABCdef123\n", strlen("ABCdef123\n")) === false) {
    echo "Не получилось выполнить socket_write(). Причина: ".socket_strerror(socket_last_error($sockets[0]));
}
if (($data = socket_read($sockets[1], strlen("ABCdef123\n"), PHP_BINARY_READ)) === false) {
    echo "Не получилось выполнить socket_read(). Причина: ".socket_strerror(socket_last_error($sockets[1]));
}
var_dump($data);

/* Закрываем сокеты */
socket_close($sockets[0]);
socket_close($sockets[1]);
?>
```

**Приклад #2 Приклад використання **socketcreatepair()** в IPC**

```php
<?php
$ary = array();
$strone = 'Сообщение от родительского процесса.';
$strtwo = 'Сообщение от дочернего процесса.';

if (socket_create_pair(AF_UNIX, SOCK_STREAM, 0, $ary) === false) {
    echo "Не получилось выполнить socket_create_pair(). Причина: ".socket_strerror(socket_last_error());
}
$pid = pcntl_fork();
if ($pid == -1) {
    echo 'Не могу создать новый процесс.';
} elseif ($pid) {
    /*родительский процесс*/
    socket_close($ary[0]);
    if (socket_write($ary[1], $strone, strlen($strone)) === false) {
        echo "Не получилось выполнить socket_write(). Причина: ".socket_strerror(socket_last_error($ary[1]));
    }
    if (socket_read($ary[1], strlen($strtwo), PHP_BINARY_READ) == $strtwo) {
        echo "Получено $strtwo\n";
    }
    socket_close($ary[1]);
} else {
    /*дочерний процесс*/
    socket_close($ary[1]);
    if (socket_write($ary[0], $strtwo, strlen($strtwo)) === false) {
        echo "Не получилось выполнить socket_write(). Причина: ".socket_strerror(socket_last_error($ary[0]));
    }
    if (socket_read($ary[0], strlen($strone), PHP_BINARY_READ) == $strone) {
        echo "Получено $strone\n";
    }
    socket_close($ary[0]);
}
?>
```

### Дивіться також

-   [socket\_create()](function.socket-create.html) - створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_create\_listen()](function.socket-create-listen.html) - Відкриває сокет на вказаному порту для прийняття з'єднань
-   [socket\_bind()](function.socket-bind.html) - Прив'язує ім'я до сокету
-   [socket\_listen()](function.socket-listen.html) - Прослуховує вхідні з'єднання на сокеті
-   [socket\_last\_error()](function.socket-last-error.html) - Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.html) - Повертає рядок, що описує помилку сокету