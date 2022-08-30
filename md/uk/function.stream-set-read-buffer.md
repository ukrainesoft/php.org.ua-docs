Встановити буферизацію читання файлу на вказаному потоці

-   [« streamsetchunksize](function.stream-set-chunk-size.html)
    
-   [streamsettimeout »](function.stream-set-timeout.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з потоками](ref.stream.html)
    
-   Встановити буферизацію читання файлу на вказаному потоці
    

# streamsetreadbuffer

(PHP 5> = 5.3.3, PHP 7, PHP 8)

streamsetreadbuffer — Встановити буферизацію читання файлу на вказаному потоці

### Опис

```methodsynopsis
stream_set_read_buffer(resource $stream, int $size): int
```

Встановлює буфер читання. Це еквівалент функції [streamsetwritebuffer()](function.stream-set-write-buffer.html), але операцій читання.

### Список параметрів

`stream`

Файловий покажчик.

`size`

Число байт для буферизації. Якщо аргумент `size` дорівнює 0, то операції читання не буферизуються. Це гарантує, що всі операції читання за допомогою функції [fread()](function.fread.html) будуть завершені до того, як іншим процесам буде дозволено читати із вхідного потоку.

### Значення, що повертаються

Повертає 0 у разі успішного виконання або інше значення, якщо запит не може бути виконаний.

### Дивіться також

-   [streamsetwritebuffer()](function.stream-set-write-buffer.html) - Встановлює буферизацію файлу під час запису у вказаний потік