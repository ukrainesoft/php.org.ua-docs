Запитує локальну сторону зазначеного сокету, в результаті можна отримати хост/порт або шлях у файловій системі Unix, залежно від типу сокету

-   [« socket\_getpeername](function.socket-getpeername.html)
    
-   [socket\_import\_stream »](function.socket-import-stream.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Запитує локальну сторону зазначеного сокету, в результаті можна отримати хост/порт або шлях у файловій системі Unix, залежно від типу сокету
    

# socketgetsockname

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketgetsockname — Запитує локальну сторону вказаного сокету, в результаті можна отримати хост/порт або шлях у файловій системі Unix, залежно від типу сокету

### Опис

```methodsynopsis
socket_getsockname(Socket $socket, string &$address, int &$port = null): bool
```

> **Зауваження**: Функція **socketgetsockname()** не повинна використовуватися із сокетами **`AF_UNIX`**, створеними за допомогою функції [socket\_connect()](function.socket-connect.html). Тільки сокети, створені функцією [socket\_accept()](function.socket-accept.html) та первинні серверні сокети після виклику [socket\_bind()](function.socket-bind.html), дозволяють отримати осмислену відповідь під час виклику цієї функції.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html), створений функцією [socket\_create()](function.socket-create.html) або [socket\_accept()](function.socket-accept.html)

`address`

Якщо заданий сокет має тип **`AF_INET`** або **`AF_INET6`** [socket\_getpeername()](function.socket-getpeername.html) поверне локальний *IP-адреса* у відповідному форматі (наприклад, `127.0.0.1` або `fe80::1`) у параметрі `address` і якщо необов'язковий параметр `port` є також пов'язаний порт.

Якщо заданий сокет має тип **`AF_UNIX`** [socket\_getpeername()](function.socket-getpeername.html) поверне шлях у файловій системі Unix (тобто . `/var/run/daemon.sock`) у параметр `address`

`port`

Якщо зазначено, то міститиме відповідний порт.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки . **socketgetsockname()** може також повертати **`false`**, якщо тип сокету не є одним з **`AF_INET`** **`AF_INET6`**, або **`AF_UNIX`**, у цьому випадку код останньої помилки сокету *не* оновлюється.

### список змін

| Версия | Описание                                                                                    |
|--------|---------------------------------------------------------------------------------------------|
|        | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_getpeername()](function.socket-getpeername.html) - Запитує віддалену сторону зазначеного сокету, в результаті може бути повернутий хост/порт або шлях у файловій системі Unix, залежно від типу сокету
-   [socket\_last\_error()](function.socket-last-error.html) - Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.html) - Повертає рядок, що описує помилку сокету