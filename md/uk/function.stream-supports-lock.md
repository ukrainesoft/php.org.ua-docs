Визначає, чи підтримує потік блокування

-   [« stream\_socket\_shutdown](function.stream-socket-shutdown.html)
    
-   [stream\_wrapper\_register »](function.stream-wrapper-register.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Визначає, чи підтримує потік блокування
    

# streamsupportslock

(PHP 5> = 5.3.0, PHP 7, PHP 8)

streamsupportslock — Визначає, чи блокування підтримує потік.

### Опис

```methodsynopsis
stream_supports_lock(resource $stream): bool
```

Визначає, чи потік підтримує блокування з використанням [flock()](function.flock.html)

### Список параметрів

`stream`

Потік для перевірки

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [flock()](function.flock.html) - Портоване консультативне блокування файлів