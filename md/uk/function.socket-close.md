---
navigation:
  - function.socket-clear-error.md: « socketclearerror
  - function.socket-cmsg-space.md: socketcmsgspace »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketclose
---
# socketclose

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketclose — Закриває екземпляр [Socket](class.socket.md)

### Опис

```methodsynopsis
socket_close(Socket $socket): void
```

Функція **socketclose()** закриває екземпляр [Socket](class.socket.md), вказаний параметром `socket`

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md)створений за допомогою функцій [socketcreate()](function.socket-create.md) або [socketaccept()](function.socket-accept.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socketbind()](function.socket-bind.md) - Прив'язує ім'я до сокету
-   [socketlisten()](function.socket-listen.md) - Прослуховує вхідні з'єднання на сокеті
-   [socketcreate()](function.socket-create.md) - створює сокет (кінцеву точку для обміну інформацією)
-   [socketstrerror()](function.socket-strerror.md) - Повертає рядок, що описує помилку сокету
