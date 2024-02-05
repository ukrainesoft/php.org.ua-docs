---
navigation:
  - function.socket-write.md: « socket\_write
  - function.socket-wsaprotocol-info-import.md: socket\_wsaprotocol\_info\_import »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_wsaprotocol\_info\_export
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_wsaprotocol\_info\_export

(PHP 7 >= 7.3.0, PHP 8)

socket\_wsaprotocol\_info\_export — Експорт структури WSAPROTOCOL\_INFO

### Опис

```methodsynopsis
socket_wsaprotocol_info_export(Socket $socket, int $process_id): string|false
```

Експортує структуру `WSAPROTOCOL_INFO` в пам'ять, що розділяється, і повертає ідентифікатор, який можна використовувати в [socket\_wsaprotocol\_info\_import()](function.socket-wsaprotocol-info-import.md). Цей ідентифікатор придатний лише для використання в процесі PID, зазначеного в `process_id`

> **Зауваження**: Функція доступна лише у Windows.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md)

`process_id`

Ідентифікатор процесу, який імпортуватиме сокет.

### Значення, що повертаються

Повертає ідентифікатор, який можна використовувати для імпорту або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_wsaprotocol\_info\_import()](function.socket-wsaprotocol-info-import.md) \- Імпортує сокет з іншого процесу
-   [socket\_wsaprotocol\_info\_release()](function.socket-wsaprotocol-info-release.md) \- Вивільняє експортовану структуру WSAPROTOCOL\_INFO
