---
navigation:
  - function.socket-recvfrom.md: « socketrecvfrom
  - function.socket-select.md: socketselect »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketrecvmsg
---
# socketrecvmsg

(PHP 5> = 5.5.0, PHP 7, PHP 8)

socketrecvmsg — Прочитати повідомлення

### Опис

```methodsynopsis
socket_recvmsg(Socket $socket, array &$message, int $flags = 0): int|false
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`socket`

`message`

`flags`

### Значення, що повертаються

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socketsendmsg()](function.socket-sendmsg.md) - Надіслати повідомлення
-   [socketcmsgspace()](function.socket-cmsg-space.md) - Обчислити розмір буфера повідомлення
