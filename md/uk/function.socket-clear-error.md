---
navigation:
  - function.socket-bind.md: « socket\_bind
  - function.socket-close.md: socket\_close »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_clear\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_clear\_error

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

socket\_clear\_error — Очищає помилку на сокеті або останній код помилки

### Опис

```methodsynopsis
socket_clear_error(?Socket $socket = null): void
```

Ця функція очищає код помилки на вказаному сокеті або останню глобальну помилку сокету, якщо не вказано.

Ця функція дозволяє примусово скинути значення коду помилки для сокету або останній глобальний код помилки модуля. Це може бути корисно для визначення всередині частини програми, чи сталася помилка ні.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socket\_create()](function.socket-create.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |
| 8.0.0 | `socket` тепер допускає значення null. |

### Дивіться також

-   [socket\_last\_error()](function.socket-last-error.md) \- Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.md) \- Повертає рядок, що описує помилку сокету
