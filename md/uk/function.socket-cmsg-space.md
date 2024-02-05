---
navigation:
  - function.socket-close.md: « socket\_close
  - function.socket-connect.md: socket\_connect »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_cmsg\_space
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_cmsg\_space

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

socket\_cmsg\_space — Визначити розмір буфера повідомлення

### Опис

```methodsynopsis
socket_cmsg_space(int $level, int $type, int $num = 0): ?int
```

Обчислює розмір буфера, який має бути виділено для отримання допоміжних даних.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`level`

`type`

### Значення, що повертаються

### Дивіться також

-   [socket\_recvmsg()](function.socket-recvmsg.md) \- Прочитати повідомлення
-   [socket\_sendmsg()](function.socket-sendmsg.md) \- Надіслати повідомлення
