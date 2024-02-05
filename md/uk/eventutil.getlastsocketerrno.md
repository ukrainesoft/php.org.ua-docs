---
navigation:
  - eventutil.construct.md: '« EventUtil::\_\_construct'
  - eventutil.getlastsocketerror.md: 'EventUtil::getLastSocketError »'
  - index.md: PHP Manual
  - class.eventutil.md: EventUtil
title: 'EventUtil::getLastSocketErrno'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventUtil::getLastSocketErrno

(PECL event >= 1.2.6-beta)

EventUtil::getLastSocketErrno — Отримати номер останньої помилки сокету, що виникла

### Опис

```methodsynopsis
public
   static
   EventUtil::getLastSocketErrno(
    mixed
     $socket
     = null
   ): int
```

Повертає номер останньої помилки сокету ( `errno`

### Список параметрів

`socket`

Ресурс сокету, потоку чи файловий дескриптор сокету.

### Значення, що повертаються

Повертає номер останньої помилки сокету ( `errno`

### Дивіться також

-   [EventUtil::getLastSocketError()](eventutil.getlastsocketerror.md) \- Отримати останню помилку сокету, що виникла
