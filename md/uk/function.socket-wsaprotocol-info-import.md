---
navigation:
  - function.socket-wsaprotocol-info-export.md: « socket\_wsaprotocol\_info\_export
  - function.socket-wsaprotocol-info-release.md: socket\_wsaprotocol\_info\_release »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_wsaprotocol\_info\_import
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_wsaprotocol\_info\_import

(PHP 7 >= 7.3.0, PHP 8)

socket\_wsaprotocol\_info\_import — імпортує сокет з іншого процесу

### Опис

```methodsynopsis
socket_wsaprotocol_info_import(string $info_id): Socket|false
```

Імпортує сокет, експортований в іншому процесі.

> **Зауваження**: Функція доступна лише у Windows.

### Список параметрів

`info_id`

Ідентифікатор, отриманий під час виклику [socket\_wsaprotocol\_info\_export()](function.socket-wsaprotocol-info-export.md)

### Значення, що повертаються

Повертає екземпляр [Socket](class.socket.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.md); раніше повертався ресурс (resource). |

### Дивіться також

-   [socket\_wsaprotocol\_info\_export()](function.socket-wsaprotocol-info-export.md) \- Експорт структури WSAPROTOCOL\_INFO
