---
navigation:
  - eventutil.getlastsocketerrno.md: '« EventUtil::getLastSocketErrno'
  - eventutil.getsocketfd.md: 'EventUtil::getSocketFd »'
  - index.md: PHP Manual
  - class.eventutil.md: EventUtil
title: 'EventUtil::getLastSocketError'
---
# EventUtil::getLastSocketError

(PECL event >= 1.2.6-beta)

EventUtil::getLastSocketError — Отримати останню помилку сокету, що виникла.

### Опис

```methodsynopsis
public
   static
   EventUtil::getLastSocketError(
    mixed
     $socket
    = ?): string
```

Повертає останню помилку сокету, що виникла.

### Список параметрів

`socket`

Ресурс сокету, потоку чи файловий дескриптор сокету.

### Значення, що повертаються

Повертає останню помилку сокету, що виникла.

### Дивіться також

-   [EventUtil::getLastSocketErrno()](eventutil.getlastsocketerrno.md) - Отримати номер останньої помилки сокету, що виникла
