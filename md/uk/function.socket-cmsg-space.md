---
navigation:
  - function.socket-close.md: « socketclose
  - function.socket-connect.md: socketconnect »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketcmsgspace
---
# socketcmsgspace

(PHP 5> = 5.5.0, PHP 7, PHP 8)

socketcmsgspace — Визначити розмір буфера повідомлення

### Опис

```methodsynopsis
socket_cmsg_space(int $level, int $type, int $num = 0): ?int
```

Обчислює розмір буфера, який має бути виділено для отримання допоміжних даних.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`level`

`type`

### Значення, що повертаються

### Дивіться також

-   [socketrecvmsg()](function.socket-recvmsg.md) - Прочитати повідомлення
-   [socketsendmsg()](function.socket-sendmsg.md) - Надіслати повідомлення
