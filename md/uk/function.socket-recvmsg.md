---
navigation:
  - function.socket-recvfrom.html: « socketrecvfrom
  - function.socket-select.html: socketselect »
  - index.html: PHP Manual
  - ref.sockets.html: Функции сокета
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
|  | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |

### Дивіться також

-   [socketsendmsg()](function.socket-sendmsg.html) - Надіслати повідомлення
-   [socketcmsgspace()](function.socket-cmsg-space.html) - Обчислити розмір буфера повідомлення
