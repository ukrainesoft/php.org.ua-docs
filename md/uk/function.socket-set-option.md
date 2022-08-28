Встановлює опції для сокету

-   [« socket\_set\_nonblock](function.socket-set-nonblock.html)
    
-   [socket\_setopt »](function.socket-setopt.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Встановлює опції для сокету
    

# socketsetoption

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

socketsetoption — Встановлює опції для сокету

### Опис

```methodsynopsis
socket_set_option(    Socket $socket,    int $level,    int $option,    array|string|int $value): bool
```

Функція **socketsetoption()** встановлює опцію, вказану в параметрі `option`, на рівні протоколу `level`у значення, вказане параметром `value` для сокету `socket`

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html), створений за допомогою функції [socket\_create()](function.socket-create.html) або [socket\_accept()](function.socket-accept.html)

`level`

Параметр `level` вказує рівень протоколу, у якому використовується опція. Наприклад, щоб встановити опції на рівні сокету, параметр `level` повинен бути встановлений у **`SOL_SOCKET`**. Інші рівні, такі як TCP, можна використовувати, вказавши номер цього рівня. Номер протоколів можна знайти за допомогою функції [getprotobyname()](function.getprotobyname.html)

`option`

Можливі опції для сокету ті самі, як і для функції [socket\_get\_option()](function.socket-get-option.html)

`value`

Значення опції.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |

### Приклади

**Приклад #1 Приклад використання **socketsetoption()****

```php
<?php
$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if (!is_resource($socket)) {
    echo 'Не могу создать сокет: '. socket_strerror(socket_last_error()) . PHP_EOL;
}

if (!socket_set_option($socket, SOL_SOCKET, SO_REUSEADDR, 1)) {
    echo 'Не могу установить опцию на сокете: '. socket_strerror(socket_last_error()) . PHP_EOL;
}

if (!socket_bind($socket, '127.0.0.1', 1223)) {
    echo 'Не могу привязать сокет: '. socket_strerror(socket_last_error()) . PHP_EOL;
}

$rval = socket_get_option($socket, SOL_SOCKET, SO_REUSEADDR);

if ($rval === false) {
    echo 'Не могу получить опцию сокета: '. socket_strerror(socket_last_error()) . PHP_EOL;
} else if ($rval !== 0) {
    echo 'Опция SO_REUSEADDR установлена на сокете!' . PHP_EOL;
}
?>
```

### Дивіться також

-   [socket\_create()](function.socket-create.html) - створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_bind()](function.socket-bind.html) - Прив'язує ім'я до сокету
-   [socket\_strerror()](function.socket-strerror.html) - Повертає рядок, що описує помилку сокету
-   [socket\_last\_error()](function.socket-last-error.html) - Повертає останню помилку на сокеті
-   [socket\_get\_option()](function.socket-get-option.html) - Отримує опції потоку для сокету