Імпортує сокет з іншого процесу

-   [« socketwsaprotocolinfoexport](function.socket-wsaprotocol-info-export.html)
    
-   [socketwsaprotocolinforelease »](function.socket-wsaprotocol-info-release.html)
    
-   [PHP Manual](index.md)
    
-   [Функции сокета](ref.sockets.md)
    
-   Імпортує сокет з іншого процесу
    

# socketwsaprotocolinfoimport

(PHP 7> = 7.3.0, PHP 8)

socketwsaprotocolinfoimport — імпортує сокет з іншого процесу

### Опис

```methodsynopsis
socket_wsaprotocol_info_import(string $info_id): Socket|false
```

Імпортує сокет, експортований в іншому процесі.

> **Зауваження**: Функція доступна лише у Windows.

### Список параметрів

`info_id`

Ідентифікатор, отриманий під час виклику [socketwsaprotocolinfoexport()](function.socket-wsaprotocol-info-export.html)

### Значення, що повертаються

Повертає екземпляр [Socket](class.socket.md) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.md); раніше повертався ресурс (resource). |

### Дивіться також

-   [socketwsaprotocolinfoexport()](function.socket-wsaprotocol-info-export.html) - Експорт структури WSAPROTOCOLINFO