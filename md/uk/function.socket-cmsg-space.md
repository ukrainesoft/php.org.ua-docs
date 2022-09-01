---
navigation:
  - function.socket-close.html: « socketclose
  - function.socket-connect.html: socketconnect »
  - index.html: PHP Manual
  - ref.sockets.html: Функции сокета
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

-   [socketrecvmsg()](function.socket-recvmsg.html) - Прочитати повідомлення
-   [socketsendmsg()](function.socket-sendmsg.html) - Надіслати повідомлення
