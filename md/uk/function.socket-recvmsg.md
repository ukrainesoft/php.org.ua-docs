---
navigation:
  - function.socket-recvfrom.md: « socket\_recvfrom
  - function.socket-select.md: socket\_select »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_recvmsg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_recvmsg

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

socket\_recvmsg — Прочитати повідомлення

### Опис

```methodsynopsis
socket_recvmsg(Socket $socket, array &$message, int $flags = 0): int|false
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`socket`

`message`

`flags`

### Значення, що повертаються

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_sendmsg()](function.socket-sendmsg.md) \- Надіслати повідомлення
-   [socket\_cmsg\_space()](function.socket-cmsg-space.md) \- Обчислити розмір буфера повідомлення
