---
navigation:
  - eventutil.getsocketname.md: '« EventUtil::getSocketName'
  - eventutil.sslrandpoll.md: 'EventUtil::sslRandPoll »'
  - index.md: PHP Manual
  - class.eventutil.md: EventUtil
title: 'EventUtil::setSocketOption'
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

Одна з констант `EventUtil::SOL_*`. Визначає рівень протоколу, до якого належить параметр. Наприклад, для роботи з рівнем сокету, параметр `level` має бути виставлений як **`EventUtil::SOL_SOCKET`**. Інші рівні, такі як TCP, можна використовувати, вказавши відповідну константу. Рівні протоколу можна переглянути за допомогою функції [getprotobyname()](function.getprotobyname.md). Дивіться [константи EventUtil](class.eventutil.md#eventutil.constants)

`optname`

Ім'я опції (тип). Те саме, що й відповідний параметр функції [socketgetoption()](function.socket-get-option.md). Дивіться [константи EventUtil](class.eventutil.md#eventutil.constants)

`optval`

Приймає ті ж значення, що й параметр `optval` функції [socketgetoption()](function.socket-get-option.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [socketgetoption()](function.socket-get-option.md) - Отримує опції потоку для сокету
-   [socketsetoption()](function.socket-set-option.md) - Встановлює опції для сокету
