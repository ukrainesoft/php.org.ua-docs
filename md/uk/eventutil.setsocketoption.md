---
navigation:
  - eventutil.getsocketname.md: '« EventUtil::getSocketName'
  - eventutil.sslrandpoll.md: 'EventUtil::sslRandPoll »'
  - index.md: PHP Manual
  - class.eventutil.md: EventUtil
title: 'EventUtil::setSocketOption'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventUtil::setSocketOption

(PECL event >= 1.6.0)

EventUtil::setSocketOption — Встановити опції сокету

### Опис

```methodsynopsis
public
   static
   EventUtil::setSocketOption(    
    mixed
     $socket
   ,    
    int
     $level
   ,    
    int
     $optname
   ,    
    mixed
     $optval
   ): bool
```

Встановлює опції сокету.

### Список параметрів

`socket`

Ресурс сокету, потоку чи файловий дескриптор, пов'язаний із сокетом.

`level`

Одна из констант`EventUtil::SOL_*`. Встановлює рівень протоколу, до якого належить параметр. Наприклад, для роботи з рівнем сокету, параметр `level` має бути виставлений як **`EventUtil::SOL_SOCKET`**. Інші рівні, такі як TCP, можна використовувати, вказавши відповідну константу. Рівні протоколу можна переглянути за допомогою функції [getprotobyname()](function.getprotobyname.md)Смотрите[константи EventUtil](class.eventutil.md#eventutil.constants)

`optname`

Ім'я опції (тип). Те саме, що й відповідний параметр функції [socket\_get\_option()](function.socket-get-option.md)Смотрите[константи EventUtil](class.eventutil.md#eventutil.constants)

`optval`

Приймає ті ж значення, що й параметр `optval` функції [socket\_get\_option()](function.socket-get-option.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [socket\_get\_option()](function.socket-get-option.md) \- Отримує опції потоку для сокету
-   [socket\_set\_option()](function.socket-set-option.md) \- Встановлює опції для сокету
