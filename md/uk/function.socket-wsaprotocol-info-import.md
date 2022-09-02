---
navigation:
  - function.socket-wsaprotocol-info-export.md: « socketwsaprotocolinfoexport
  - function.socket-wsaprotocol-info-release.md: socketwsaprotocolinforelease »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketwsaprotocolinfoimport
---
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

Ідентифікатор, отриманий під час виклику [socketwsaprotocolinfoexport()](function.socket-wsaprotocol-info-export.md)

### Значення, що повертаються

Повертає екземпляр [Socket](class.socket.md) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.md); раніше повертався ресурс (resource). |

### Дивіться також

-   [socketwsaprotocolinfoexport()](function.socket-wsaprotocol-info-export.md) - Експорт структури WSAPROTOCOLINFO
