Експорт структури WSAPROTOCOLINFO

-   [« socket\_write](function.socket-write.html)
    
-   [socket\_wsaprotocol\_info\_import »](function.socket-wsaprotocol-info-import.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Експорт структури WSAPROTOCOLINFO
    

# socketwsaprotocolinfoexport

(PHP 7> = 7.3.0, PHP 8)

socketwsaprotocolinfoexport — Експорт структури WSAPROTOCOLINFO

### Опис

```methodsynopsis
socket_wsaprotocol_info_export(Socket $socket, int $process_id): string|false
```

Експортує структуру `WSAPROTOCOL_INFO` в пам'ять, що розділяється, і повертає ідентифікатор, який можна використовувати в [socket\_wsaprotocol\_info\_import()](function.socket-wsaprotocol-info-import.html). Цей ідентифікатор придатний лише для використання в процесі PID, зазначеного в `process_id`

> **Зауваження**: Функція доступна лише у Windows.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html)

`process_id`

Ідентифікатор процесу, який імпортуватиме сокет.

### Значення, що повертаються

Повертає ідентифікатор, який можна використовувати для імпорту або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                    |
|--------|---------------------------------------------------------------------------------------------|
|        | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_wsaprotocol\_info\_import()](function.socket-wsaprotocol-info-import.html) - Імпортує сокет з іншого процесу
-   [socket\_wsaprotocol\_info\_release()](function.socket-wsaprotocol-info-release.html) - Вивільняє експортовану структуру WSAPROTOCOLINFO