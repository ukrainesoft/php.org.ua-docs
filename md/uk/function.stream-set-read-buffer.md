---
navigation:
  - function.stream-set-chunk-size.md: « stream\_set\_chunk\_size
  - function.stream-set-timeout.md: stream\_set\_timeout »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_set\_read\_buffer
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_set\_read\_buffer

(PHP 5 >= 5.3.3, PHP 7, PHP 8)

stream\_set\_read\_buffer — Встановити буферизацію читання файлу на вказаному потоці

### Опис

```methodsynopsis
stream_set_read_buffer(resource $stream, int $size): int
```

Встановлює буфер читання. Це еквівалент функції [stream\_set\_write\_buffer()](function.stream-set-write-buffer.md), але операцій читання.

### Список параметрів

`stream`

Файловий покажчик.

`size`

Число байт для буферизации. Если аргумент`size` дорівнює 0, то операції читання не буферизуються. Це гарантує, що всі операції читання за допомогою функції [fread()](function.fread.md) будуть завершені до того, як іншим процесам буде дозволено читати із вхідного потоку.

### Значення, що повертаються

Повертає 0 у разі успішного виконання або інше значення, якщо запит не може бути виконаний.

### Дивіться також

-   [stream\_set\_write\_buffer()](function.stream-set-write-buffer.md) \- Встановлює буферизацію файлу під час запису у вказаний потік
