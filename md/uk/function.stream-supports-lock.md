---
navigation:
  - function.stream-socket-shutdown.md: « stream\_socket\_shutdown
  - function.stream-wrapper-register.md: stream\_wrapper\_register »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_supports\_lock
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_supports\_lock

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

stream\_supports\_lock — Визначає, чи блокування підтримує потік.

### Опис

```methodsynopsis
stream_supports_lock(resource $stream): bool
```

Визначає, чи потік підтримує блокування з використанням [flock()](function.flock.md)

### Список параметрів

`stream`

Потік для перевірки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [flock()](function.flock.md) \- Портоване консультативне блокування файлів
