---
navigation:
  - function.socket-getpeername.md: « socket\_getpeername
  - function.socket-import-stream.md: socket\_import\_stream »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_getsockname
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_getsockname

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_getsockname — Запитує локальну сторону вказаного сокету, в результаті можна отримати хост/порт або шлях у файловій системі Unix, залежно від типу сокету

### Опис

```methodsynopsis
socket_getsockname(Socket $socket, string &$address, int &$port = null): bool
```

> **Зауваження**: Функция**socket\_getsockname()** не повинна використовуватися із сокетами **`AF_UNIX`**, створеними за допомогою функції [socket\_connect()](function.socket-connect.md). Тільки сокети, створені функцією [socket\_accept()](function.socket-accept.md) та первинні серверні сокети після виклику [socket\_bind()](function.socket-bind.md), дозволяють отримати осмислену відповідь під час виклику цієї функції.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений функцією [socket\_create()](function.socket-create.md) або [socket\_accept()](function.socket-accept.md)

`address`

Якщо заданий сокет має тип **`AF_INET`** або **`AF_INET6`** [socket\_getpeername()](function.socket-getpeername.md) поверне локальний *IP-адреса* у відповідному форматі (наприклад, `127.0.0.1`или`fe80::1`) в параметре`address` і якщо необов'язковий параметр `port` є також пов'язаний порт.

Якщо заданий сокет має тип **`AF_UNIX`** [socket\_getpeername()](function.socket-getpeername.md) поверне шлях у файловій системі Unix (тобто . `/var/run/daemon.sock`) в параметр`address`

`port`

Якщо зазначено, то міститиме відповідний порт.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`**в случае возникновения ошибки**socket\_getsockname()** може також повертати **`false`**, якщо тип сокету не є одним з **`AF_INET`** **`AF_INET6`**, или\*\*`AF_UNIX`\*\*, у цьому випадку код останньої помилки сокету *не* оновлюється.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_getpeername()](function.socket-getpeername.md) \- Запитує віддалену сторону зазначеного сокету, в результаті може бути повернутий хост/порт або шлях у файловій системі Unix, залежно від типу сокету
-   [socket\_last\_error()](function.socket-last-error.md) \- Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.md) \- Повертає рядок, що описує помилку сокету
