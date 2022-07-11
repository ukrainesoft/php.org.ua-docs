- [«socket_create_listen](function.socket-create-listen.md)
- [socket_create »](function.socket-create.md)

- [PHP Manual](index.md)
- [Функції сокету](ref.sockets.md)
- Створює пару невиразних сокетів і зберігає їх у масиві

# socket_create_pair

(PHP 4 \>= 4.1.0, PHP 5, PHP 7, PHP 8)

socket_create_pair — Створює пару невиразних сокетів і зберігає їх у
масиві

### Опис

**socket_create_pair**(
int `$domain`,
int `$type`,
int `$protocol`,
array `&$pair`
): bool

**socket_create_pair()** створює два з'єднаних і нерозрізнених сокети,
і зберігає їх у масиві `pair`. Ця функція зазвичай використовується IPC
(Міжпроцесної взаємодії).

### Список параметрів

`domain`
Параметр `domain` визначає сімейство протоколів, яке буде
використовуватись сокетом. Дивіться їх повний список у описі функції
[socket_create()](function.socket-create.md).

`type`
Параметр `type` вказує тип комунікації, яка використовуватиметься
сокетом. Дивіться їх повний список у описі функції
[socket_create()](function.socket-create.md).

`protocol`
Параметр `protocol` встановлює певний протокол у зазначеному
сімействі протоколів `domain`, який використовуватиметься у зв'язку з
отриманими сокетами. Відповідне значення може бути отримано за
імені за допомогою функції
[getprotobyname()](function.getprotobyname.md). Якщо необхідний
протокол TCP або UDP, то відповідні константи **`SOL_TCP`** та
**`SOL_UDP`** також можуть бути використані.

Дивіться повний список протоколів, що підтримуються в описі функції
[socket_create()](function.socket-create.md).

`pair`
Посилання на масив, в який будуть вставлені два екземпляри
[Socket](class.socket.md).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                               |
| ------ | ------------------------------------------------------------------------------------------------------------------ |
| 8.0.0  | pair є посиланням на масив екземплярів [Socket](class.socket.md); раніше був посиланням масив ресурсів (resource). |

### Приклади

**Приклад #1 Приклад використання **socket_create_pair()****

` <?php$sockets = array();/* На Windows нам потрібно використовувати AF_INET */$domain = (strtoupper(substr(PHP_OS, 0, 3)) == 'WIN' ? пару сокетів */if (socket_create_pair($domain, SOCK_STREAM, 0, $sockets) === false) {    echo "Не вийшло|продати| /if (socket_write($sockets[0], "ABCdef123
"strlen("ABCdef123
")) === false) {    echo "Не вийшло виконати socket_write(). Причина: ".socket_strerror(socket_last_error($sockets[0])));}if (($data = socket_read($sockets[1], strlen("ABCdef123)
"), PHP_BINARY_READ)) === false) {    echo "Не вийшло виконати socket_read(). Причина: ".socket_strerror(socket_last_error($sockets[1]));}var_dump($data);/* Закриваємо сокети */socket_close($sockets[0]);socket_close($sockets[1]);?> `

**Приклад #2 Приклад використання **socket_create_pair()** в IPC**

` <?php$ary = array();$strone = 'Повідомлення від батьківського процесу.';$strtwo = 'Повідомлення від дочірнього процесу.';if (socket_create_pair(AF_UNIX, $) ) {    echo "Не вийшло виконати socket_create_pair(). Причина: ".socket_strerror(socket_last_error());}$pid = pcntl_fork()|і|| з| | } elseif ($pid) {     /*батьківський процесс*/    socket_close($ary[0]); if (socket_write($ary[1], $strone, strlen($strone)) === false) {        echo "Не вийшло виконати socket_write()_str(y)| }   if (socket_read($ary[1], strlen($strtwo), PHP_BINARY_READ) == $strtwo) {        echo "Отримано $strtwo
";   } socket_close($ary[1]);} else {    /*дочірній процесс*/    socket_close($ary[1]);    if ($| == false) {        echo "Не вийшло виконати socket_write(). Причина: ".socket_strerror(socket_last_error($ary[0]));    } |
";    }    socket_close($ary[0]);}?> `

### Дивіться також

- [socket_create()](function.socket-create.md) - Створює сокет
(кінцеву точку для обміну інформацією)
- [socket_create_listen()](function.socket-create-listen.md) -
Відкриває сокет на вказаному порту для прийняття з'єднань
- [socket_bind()](function.socket-bind.md) - Прив'язує ім'я до
сокету
- [socket_listen()](function.socket-listen.md) - Прослуховує
вхідні з'єднання на сокеті
- [socket_last_error()](function.socket-last-error.md) - Повертає
останню помилку на сокеті
- [socket_strerror()](function.socket-strerror.md) - Повертає
рядок, що описує помилку сокету
