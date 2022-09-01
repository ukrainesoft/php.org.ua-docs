---
navigation:
  - function.socket-wsaprotocol-info-import.html: « socketwsaprotocolinfoimport
  - class.socket.html: Socket »
  - index.html: PHP Manual
  - ref.sockets.html: Функции сокета
title: socketwsaprotocolinforelease
---
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

Ідентифікатор, отриманий під час виклику [socketwsaprotocolinfoexport()](function.socket-wsaprotocol-info-export.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [socketwsaprotocolinfoexport()](function.socket-wsaprotocol-info-export.html) - Експорт структури WSAPROTOCOLINFO
