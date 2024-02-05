---
navigation:
  - function.socket-wsaprotocol-info-import.md: « socket\_wsaprotocol\_info\_import
  - class.socket.md: Socket »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_wsaprotocol\_info\_release
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_wsaprotocol\_info\_release

(PHP 7 >= 7.3.0, PHP 8)

socket\_wsaprotocol\_info\_release — Вивільняє експортовану структуру WSAPROTOCOL\_INFO

### Опис

```methodsynopsis
socket_wsaprotocol_info_release(string $info_id): bool
```

Вивільняє пам'ять, що розділяється, відповідну заданому `info_id`

> **Зауваження**: Функція доступна лише у Windows.

### Список параметрів

`info_id`

Ідентифікатор, отриманий під час виклику [socket\_wsaprotocol\_info\_export()](function.socket-wsaprotocol-info-export.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [socket\_wsaprotocol\_info\_export()](function.socket-wsaprotocol-info-export.md) \- Експорт структури WSAPROTOCOL\_INFO
