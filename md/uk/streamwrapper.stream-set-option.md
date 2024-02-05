---
navigation:
  - streamwrapper.stream-seek.md: '« streamWrapper::stream\_seek'
  - streamwrapper.stream-stat.md: 'streamWrapper::stream\_stat »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_set\_option'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_set\_option

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

streamWrapper::stream\_set\_option — Зміна налаштувань потоку

### Опис

```methodsynopsis
public streamWrapper::stream_set_option(int $option, int $arg1, int $arg2): bool
```

Цей метод викликається під час встановлення параметрів потоку.

### Список параметрів

`option`

Одне із значень:

-   **`STREAM_OPTION_BLOCKING`**(Метод викликаний у результаті виклику функції[stream\_set\_blocking()](function.stream-set-blocking.md)) .
-   **`STREAM_OPTION_READ_TIMEOUT`**(Метод викликаний у результаті виклику функції[stream\_set\_timeout()](function.stream-set-timeout.md)) .
-   **`STREAM_OPTION_WRITE_BUFFER`**(Метод викликаний у результаті виклику функції[stream\_set\_write\_buffer()](function.stream-set-write-buffer.md)) .

`arg1`

Якщо `option`принимает значение:

-   **`STREAM_OPTION_BLOCKING`**: запит режиму блокування (1 - блокувати, 0 - не блокувати).
-   **`STREAM_OPTION_READ_TIMEOUT`**: час очікування в секундах
-   **`STREAM_OPTION_WRITE_BUFFER`**: режим буферизації (**`STREAM_BUFFER_NONE`** або **`STREAM_BUFFER_FULL`**

`arg2`

Якщо `option`принимает значение:

-   **`STREAM_OPTION_BLOCKING`**: це значення ні на що не впливає
-   **`STREAM_OPTION_READ_TIMEOUT`**: час очікування у мілісекундах.
-   **`STREAM_OPTION_WRITE_BUFFER`**: потрібний розмір буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`**в случае возникновения ошибки. Если`option`не реализован, метод должен возвращать**`false`**

### Дивіться також

-   [stream\_set\_blocking()](function.stream-set-blocking.md) \- Встановити блокуючий/неблокуючий режим у потоці
-   [stream\_set\_timeout()](function.stream-set-timeout.md) \- Встановити значення часу очікування потоку
-   [stream\_set\_write\_buffer()](function.stream-set-write-buffer.md) \- Встановлює буферизацію файлу під час запису у вказаний потік
