---
navigation:
  - function.socket-send.html: « socketsend
  - function.socket-sendto.html: socketsendto »
  - index.html: PHP Manual
  - ref.sockets.html: Функции сокета
title: socketsendmsg
---
# socketsendmsg

(PHP 5> = 5.5.0, PHP 7, PHP 8)

socketsendmsg — Надіслати повідомлення

### Опис

```methodsynopsis
socket_sendmsg(Socket $socket, array $message, int $flags = 0): int|false
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`socket`

`message`

`flags`

### Значення, що повертаються

Повертає кількість відправлених байтів або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socketrecvmsg()](function.socket-recvmsg.md) - Прочитати повідомлення
-   [socketcmsgspace()](function.socket-cmsg-space.md) - Обчислити розмір буфера повідомлення
