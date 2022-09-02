---
navigation:
  - function.socket-getopt.md: « socketgetopt
  - function.socket-getsockname.md: socketgetsockname »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketgetpeername
---
# socketgetpeername

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketgetpeername — Запитує віддалену сторону зазначеного сокету, в результаті може бути повернутий хост/порт або шлях у файловій системі Unix, залежно від типу сокету

### Опис

```methodsynopsis
socket_getpeername(Socket $socket, string &$address, int &$port = null): bool
```

Запитує віддалену сторону зазначеного сокету, в результаті може бути повернено хост/порт або шлях у файловій системі Unix, залежно від типу сокету.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socketcreate()](function.socket-create.md) або [socketaccept()](function.socket-accept.md)

`address`

Якщо заданий сокет має тип **`AF_INET`** або **`AF_INET6`** **socketgetpeername()** поверне віддалений *IP-адреса* у відповідному форматі (наприклад, `127.0.0.1` або `fe80::1`) у параметрі `address` і якщо необов'язковий параметр `port` є також пов'язаний порт.

Якщо заданий сокет має тип **`AF_UNIX`** **socketgetpeername()** поверне шлях у файловій системі Unix (тобто . `/var/run/daemon.sock`) у параметр `address`

`port`

Якщо зазначено, то міститиме порт, пов'язаний з адресою `address`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки . **socketgetpeername()** також може повернути \*\*`false`\*\*якщо сокет мати тип відмінний від **`AF_INET`** **`AF_INET6`** або **`AF_UNIX`**, у цьому випадку код останньої помилки сокету *НЕ* буде оновлено.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Примітки

> **Зауваження**
> 
> **socketgetpeername()** не повинна бути використана із сокетами **`AF_UNIX`**, створеними за допомогою функції [socketaccept()](function.socket-accept.md). Тільки сокети, створені за допомогою [socketconnect()](function.socket-connect.md) або серверний сокет, до якого застосовано виклик функції [socketbind()](function.socket-bind.md), повертатимуть осмислені значення.

> **Зауваження**
> 
> Для того щоб **socketgetpeername()** повернула осмислене значення, сокет, якого вона застосовується, повинен розуміти концепцію " рівних відносин " (peer).

### Дивіться також

-   [socketgetsockname()](function.socket-getsockname.md) - Запитує локальну сторону зазначеного сокету, в результаті можна отримати хост/порт або шлях у файловій системі Unix, залежно від типу сокету
-   [socketlasterror()](function.socket-last-error.md) - Повертає останню помилку на сокеті
-   [socketstrerror()](function.socket-strerror.md) - Повертає рядок, що описує помилку сокету
