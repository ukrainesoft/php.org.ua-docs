---
navigation:
  - function.stream-socket-shutdown.md: « streamsocketshutdown
  - function.stream-wrapper-register.md: streamwrapperregister »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamsupportslock
---
# streamsupportslock

(PHP 5> = 5.3.0, PHP 7, PHP 8)

streamsupportslock — Визначає, чи блокування підтримує потік.

### Опис

```methodsynopsis
stream_supports_lock(resource $stream): bool
```

Визначає, чи потік підтримує блокування з використанням [flock()](function.flock.md)

### Список параметрів

`stream`

Потік для перевірки

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [flock()](function.flock.md) - Портоване консультативне блокування файлів
