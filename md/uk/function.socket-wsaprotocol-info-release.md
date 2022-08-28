Вивільняє експортовану структуру WSAPROTOCOLINFO

-   [« socket\_wsaprotocol\_info\_import](function.socket-wsaprotocol-info-import.html)
    
-   [Socket »](class.socket.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Вивільняє експортовану структуру WSAPROTOCOLINFO
    

# socketwsaprotocolinforelease

(PHP 7> = 7.3.0, PHP 8)

socketwsaprotocolinforelease — Вивільняє експортовану структуру WSAPROTOCOLINFO

### Опис

```methodsynopsis
socket_wsaprotocol_info_release(string $info_id): bool
```

Вивільняє пам'ять, що розділяється, відповідну заданому `info_id`

> **Зауваження**: Функція доступна лише у Windows.

### Список параметрів

`info_id`

Ідентифікатор, отриманий під час виклику [socket\_wsaprotocol\_info\_export()](function.socket-wsaprotocol-info-export.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [socket\_wsaprotocol\_info\_export()](function.socket-wsaprotocol-info-export.html) - Експорт структури WSAPROTOCOLINFO