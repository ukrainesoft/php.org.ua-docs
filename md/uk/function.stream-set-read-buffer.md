---
navigation:
  - function.stream-set-chunk-size.md: « streamsetchunksize
  - function.stream-set-timeout.md: streamsettimeout »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamsetreadbuffer
---
# streamsetreadbuffer

(PHP 5> = 5.3.3, PHP 7, PHP 8)

streamsetreadbuffer — Встановити буферизацію читання файлу на вказаному потоці

### Опис

```methodsynopsis
stream_set_read_buffer(resource $stream, int $size): int
```

Встановлює буфер читання. Це еквівалент функції [streamsetwritebuffer()](function.stream-set-write-buffer.md), але операцій читання.

### Список параметрів

`stream`

Файловий покажчик.

`size`

Число байт для буферизації. Якщо аргумент `size` дорівнює 0, то операції читання не буферизуються. Це гарантує, що всі операції читання за допомогою функції [fread()](function.fread.md) будуть завершені до того, як іншим процесам буде дозволено читати із вхідного потоку.

### Значення, що повертаються

Повертає 0 у разі успішного виконання або інше значення, якщо запит не може бути виконаний.

### Дивіться також

-   [streamsetwritebuffer()](function.stream-set-write-buffer.md) - Встановлює буферизацію файлу під час запису у вказаний потік
