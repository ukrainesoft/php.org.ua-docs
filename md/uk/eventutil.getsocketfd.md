---
navigation:
  - eventutil.getlastsocketerror.md: '« EventUtil::getLastSocketError'
  - eventutil.getsocketname.md: 'EventUtil::getSocketName »'
  - index.md: PHP Manual
  - class.eventutil.md: EventUtil
title: 'EventUtil::getSocketFd'
---
# EventUtil::getSocketFd

(PECL event >= 1.7.0)

EventUtil::getSocketFd — Отримати числовий файловий дескриптор сокету або потоку

### Опис

```methodsynopsis
public
   static
   EventUtil::getSocketFd(
    mixed
     $socket
   ): int
```

Повертає числовий файловий дескриптор сокета чи потоку, заданий параметром `socket`, так само як це робить модуль `Event` для всіх методів, які приймають ресурси сокету чи потоку.

### Список параметрів

`socket`

Ресурс сокету чи потоку.

### Значення, що повертаються

Повертає числовий файловий дескриптор . **EventUtil::getSocketFd()** повертає **`false`**, якщо не вдалося визначити тип файлу нижче, або якщо файловий дескриптор, пов'язаний з `socket` некоректний.
