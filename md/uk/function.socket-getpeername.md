---
navigation:
  - function.socket-getopt.md: « socket\_getopt
  - function.socket-getsockname.md: socket\_getsockname »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_getpeername
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_getpeername

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_getpeername — Запитує віддалену сторону зазначеного сокету, в результаті може бути повернутий хост/порт або шлях у файловій системі Unix, залежно від типу сокету

### Опис

```methodsynopsis
socket_getpeername(Socket $socket, string &$address, int &$port = null): bool
```

Запитує віддалену сторону зазначеного сокету, в результаті може бути повернутий хост/порт або шлях у файловій системі Unix, залежно від типу сокету.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socket\_create()](function.socket-create.md) або [socket\_accept()](function.socket-accept.md)

`address`

Якщо заданий сокет має тип **`AF_INET`** або **`AF_INET6`** **socket\_getpeername()** поверне віддалений *IP-адреса* у відповідному форматі (наприклад, `127.0.0.1`или`fe80::1`) в параметре`address` і якщо необов'язковий параметр `port` є також пов'язаний порт.

Якщо заданий сокет має тип **`AF_UNIX`** **socket\_getpeername()** поверне шлях у файловій системі Unix (тобто . `/var/run/daemon.sock`) в параметр`address`

`port`

Якщо зазначено, то міститиме порт, пов'язаний з адресою `address`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`**в случае возникновения ошибки**socket\_getpeername()** також може повернути \*\*`false`\*\*якщо сокет мати тип відмінний від **`AF_INET`** **`AF_INET6`** або **`AF_UNIX`**, у цьому випадку код останньої помилки сокету *НЕ* буде оновлено.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Примітки

> **Зауваження** :
> 
> **socket\_getpeername()** не повинна бути використана із сокетами **`AF_UNIX`**, створеними за допомогою функції [socket\_accept()](function.socket-accept.md). Тільки сокети, створені за допомогою [socket\_connect()](function.socket-connect.md) або серверний сокет, до якого застосовано виклик функції [socket\_bind()](function.socket-bind.md), повертатимуть осмислені значення.

> **Зауваження** :
> 
> Для того щоб **socket\_getpeername()** повернула осмислене значення, сокет, якого вона застосовується, повинен розуміти концепцію " рівних відносин " (peer).

### Дивіться також

-   [socket\_getsockname()](function.socket-getsockname.md) \- Запитує локальну сторону зазначеного сокету, в результаті можна отримати хост/порт або шлях у файловій системі Unix, залежно від типу сокету
-   [socket\_last\_error()](function.socket-last-error.md) \- Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.md) \- Повертає рядок, що описує помилку сокету
