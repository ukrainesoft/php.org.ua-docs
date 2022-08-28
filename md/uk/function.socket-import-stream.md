Імпортувати потік

-   [« socket\_getsockname](function.socket-getsockname.html)
    
-   [socket\_last\_error »](function.socket-last-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Імпортувати потік
    

# socketimportstream

(PHP 5> = 5.4.0, PHP 7, PHP 8)

socketimportstream — Імпортувати потік

### Опис

```methodsynopsis
socket_import_stream(resource $stream): Socket|false
```

Імпортує потік, який інкапсулює сокет ресурс модуля сокету.

### Список параметрів

`stream`

Ресурс потік імпорту.

### Значення, що повертаються

Повертає **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.html); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **socketimportstream()****

```php
<?php
$stream = stream_socket_server("udp://0.0.0.0:58380", $errno, $errstr, STREAM_SERVER_BIND);
$sock   = socket_import_stream($stream);
?>
```

### Дивіться також

-   [stream\_socket\_server()](function.stream-socket-server.html) - Створює інтернет-сокет або доменний сокет Unix