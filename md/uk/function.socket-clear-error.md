---
navigation:
  - function.socket-bind.md: « socketbind
  - function.socket-close.md: socketclose »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketclearerror
---
# socketclearerror

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

socketclearerror — Очищає помилку на сокеті або останній код помилки

### Опис

```methodsynopsis
socket_clear_error(?Socket $socket = null): void
```

Ця функція очищає код помилки на вказаному сокеті або останню глобальну помилку сокету, якщо сокет не вказано.

Ця функція дозволяє примусово скинути значення коду помилки для сокету або останній глобальний код помилки модуля. Це може бути корисно для визначення всередині частини програми, чи сталася помилка ні.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socketcreate()](function.socket-create.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |
|  | `socket` тепер допускає значення null. |

### Дивіться також

-   [socketlasterror()](function.socket-last-error.md) - Повертає останню помилку на сокеті
-   [socketstrerror()](function.socket-strerror.md) - Повертає рядок, що описує помилку сокету
