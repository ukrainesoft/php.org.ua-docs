Зміна налаштувань потоку

-   [« streamWrapper::streamseek](streamwrapper.stream-seek.html)
    
-   [streamWrapper::streamstat »](streamwrapper.stream-stat.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Зміна налаштувань потоку
    

# streamWrapper::streamsetoption

(PHP 5> = 5.3.0, PHP 7, PHP 8)

streamWrapper::streamsetoption — Змінити параметри потоку.

### Опис

```methodsynopsis
public streamWrapper::stream_set_option(int $option, int $arg1, int $arg2): bool
```

Цей метод викликається під час встановлення параметрів потоку.

### Список параметрів

`option`

Одне із значень:

-   **`STREAM_OPTION_BLOCKING`** (Метод викликаний у результаті виклику функції [streamsetblocking()](function.stream-set-blocking.html)
-   **`STREAM_OPTION_READ_TIMEOUT`** (Метод викликаний у результаті виклику функції [streamsettimeout()](function.stream-set-timeout.html)
-   **`STREAM_OPTION_WRITE_BUFFER`** (Метод викликаний у результаті виклику функції [streamsetwritebuffer()](function.stream-set-write-buffer.html)

`arg1`

Якщо `option` набуває значення:

-   **`STREAM_OPTION_BLOCKING`**: запит режиму блокування (1 - блокувати, 0 - не блокувати).
-   **`STREAM_OPTION_READ_TIMEOUT`**: час очікування в секундах
-   **`STREAM_OPTION_WRITE_BUFFER`**: режим буферизації (**`STREAM_BUFFER_NONE`** або **`STREAM_BUFFER_FULL`**

`arg2`

Якщо `option` набуває значення:

-   **`STREAM_OPTION_BLOCKING`**: це значення ні на що не впливає
-   **`STREAM_OPTION_READ_TIMEOUT`**: час очікування у мілісекундах.
-   **`STREAM_OPTION_WRITE_BUFFER`**: потрібний розмір буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо `option` не реалізований, метод має повертати **`false`**

### Дивіться також

-   [streamsetblocking()](function.stream-set-blocking.html) - Встановити блокуючий/неблокуючий режим у потоці
-   [streamsettimeout()](function.stream-set-timeout.html) - Встановити значення часу очікування потоку
-   [streamsetwritebuffer()](function.stream-set-write-buffer.html) - Встановлює буферизацію файлу під час запису у вказаний потік