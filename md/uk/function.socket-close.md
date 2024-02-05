---
navigation:
  - function.socket-clear-error.md: « socket\_clear\_error
  - function.socket-cmsg-space.md: socket\_cmsg\_space »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_close

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_close — Закриває екземпляр [Socket](class.socket.md)

### Опис

```methodsynopsis
socket_close(Socket $socket): void
```

Функция**socket\_close()** закриває екземпляр [Socket](class.socket.md), вказаний параметром `socket`

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md)створений за допомогою функцій [socket\_create()](function.socket-create.md) або [socket\_accept()](function.socket-accept.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_bind()](function.socket-bind.md) \- Прив'язує ім'я до сокету
-   [socket\_listen()](function.socket-listen.md) \- Прослуховує вхідні з'єднання на сокеті
-   [socket\_create()](function.socket-create.md) \- створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_strerror()](function.socket-strerror.md) \- Повертає рядок, що описує помилку сокету
