---
navigation:
  - function.socket-import-stream.md: « socket\_import\_stream
  - function.socket-listen.md: socket\_listen »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_last\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_last\_error

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_last\_error — Повертає останню помилку на сокеті

### Опис

```methodsynopsis
socket_last_error(?Socket $socket = null): int
```

Якщо екземпляр [Socket](class.socket.md) передано цю функцію, то повертається остання помилка, яка сталася на цьому конкретному сокеті. Якщо `socket` не вказано, повертається код помилки останньої функції сокетів. Останнє особливо корисне для таких функцій, як [socket\_create()](function.socket-create.md), яка не повертає сокет у разі невдачі та [socket\_select()](function.socket-select.md), яка може закінчитися невдало з причин, не пов'язаних безпосередньо з конкретним сокетом. Код помилки підходить для передачі функції [socket\_strerror()](function.socket-strerror.md), яка повертає рядок, що описує вказаний код помилки.

Якщо помилок немає або вони були очищені функцією [socket\_clear\_error()](function.socket-clear-error.md), функція поверне

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socket\_create()](function.socket-create.md)

### Значення, що повертаються

Ця функція повертає код помилки сокету.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |
| 8.0.0 | `socket` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**socket\_last\_error()\*\*\*\*

```php
<?php
$socket = @socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if ($socket === false) {
    $errorcode = socket_last_error();
    $errormsg = socket_strerror($errorcode);

    die("Не могу создать сокет: [$errorcode] $errormsg");
}
?>
```

### Примітки

> **Зауваження** :
> 
> \*\*socket\_last\_error()\*\*не очищает код ошибки, используйте[socket\_clear\_error()](function.socket-clear-error.md) для цієї мети.
