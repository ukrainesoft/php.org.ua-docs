---
navigation:
  - function.socket-getsockname.md: « socket\_getsockname
  - function.socket-last-error.md: socket\_last\_error »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_import\_stream
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_import\_stream

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

socket\_import\_stream — Імпортувати потік

### Опис

```methodsynopsis
socket_import_stream(resource $stream): Socket|false
```

Імпортує потік, який інкапсулює сокет ресурс модуля сокету.

### Список параметрів

`stream`

Ресурс потік імпорту.

### Значення, що повертаються

Повертає \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.md); раніше повертався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**socket\_import\_stream()\*\*\*\*

```php
<?php
$stream = stream_socket_server("udp://0.0.0.0:58380", $errno, $errstr, STREAM_SERVER_BIND);
$sock   = socket_import_stream($stream);
?>
```

### Дивіться також

-   [stream\_socket\_server()](function.stream-socket-server.md) \- Створює інтернет-сокет або доменний сокет Unix
