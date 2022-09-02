---
navigation:
  - function.socket-set-nonblock.md: « socketsetnonblock
  - function.socket-setopt.md: socketsetopt »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketsetoption
---
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

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socketcreate()](function.socket-create.md) або [socketaccept()](function.socket-accept.md)

`level`

Параметр `level` вказує рівень протоколу, у якому використовується опція. Наприклад, щоб встановити опції на рівні сокету, параметр `level` повинен бути встановлений у **`SOL_SOCKET`**. Інші рівні, такі як TCP, можна використовувати, вказавши номер цього рівня. Номер протоколів можна знайти за допомогою функції [getprotobyname()](function.getprotobyname.md)

`option`

Можливі опції для сокету ті самі, як і для функції [socketgetoption()](function.socket-get-option.md)

`value`

Значення опції.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

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

-   [socketcreate()](function.socket-create.md) - створює сокет (кінцеву точку для обміну інформацією)
-   [socketbind()](function.socket-bind.md) - Прив'язує ім'я до сокету
-   [socketstrerror()](function.socket-strerror.md) - Повертає рядок, що описує помилку сокету
-   [socketlasterror()](function.socket-last-error.md) - Повертає останню помилку на сокеті
-   [socketgetoption()](function.socket-get-option.md) - Отримує опції потоку для сокету
