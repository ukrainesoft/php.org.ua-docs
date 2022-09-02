---
navigation:
  - function.socket-import-stream.md: « socketimportstream
  - function.socket-listen.md: socketlisten »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketlasterror
---
# socketlasterror

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketlasterror — Повертає останню помилку на сокеті

### Опис

```methodsynopsis
socket_last_error(?Socket $socket = null): int
```

Якщо екземпляр [Socket](class.socket.md) передано цю функцію, то повертається остання помилка, яка сталася на цьому конкретному сокеті. Якщо `socket` не вказано, повертається код помилки останньої функції сокетів. Останнє особливо корисне для таких функцій, як [socketcreate()](function.socket-create.md), яка не повертає сокет у разі невдачі та [socketselect()](function.socket-select.md), що може закінчитися невдало з причин, не пов'язаних безпосередньо з конкретним сокетом. Код помилки підходить для передачі функції [socketstrerror()](function.socket-strerror.md), яка повертає рядок, що описує вказаний код помилки.

Якщо помилок немає або вони були очищені функцією [socketclearerror()](function.socket-clear-error.md), функція поверне `0`

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socketcreate()](function.socket-create.md)

### Значення, що повертаються

Ця функція повертає код помилки сокету.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |
|  | `socket` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **socketlasterror()****

```php
<?php
$socket = @socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if ($socket === false) {
    $errorcode = socket_last_error();
    $errormsg = socket_strerror($errorcode);

    die("Не могу создать сокет: [$errorcode] $errormsg");
}
?>
```

### Примітки

> **Зауваження**
> 
> **socketlasterror()** не очищає код помилки, використовуйте [socketclearerror()](function.socket-clear-error.md) для цієї мети.
