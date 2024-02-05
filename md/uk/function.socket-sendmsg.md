---
navigation:
  - function.socket-send.md: « socket\_send
  - function.socket-sendto.md: socket\_sendto »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_sendmsg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_sendmsg

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

socket\_sendmsg — Надіслати повідомлення

### Опис

```methodsynopsis
socket_sendmsg(Socket $socket, array $message, int $flags = 0): int|false
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`socket`

`message`

`flags`

### Значення, що повертаються

Повертає кількість відправлених байтів або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_recvmsg()](function.socket-recvmsg.md) \- Прочитати повідомлення
-   [socket\_cmsg\_space()](function.socket-cmsg-space.md) \- Обчислити розмір буфера повідомлення
