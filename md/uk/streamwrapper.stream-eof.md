Перевіряє досягнення кінця файлу за файловим покажчиком

-   [« streamWrapper::stream\_close](streamwrapper.stream-close.html)
    
-   [streamWrapper::stream\_flush »](streamwrapper.stream-flush.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Перевіряє досягнення кінця файлу за файловим покажчиком
    

# streamWrapper::streameof

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::streameof — Перевіряє досягнення кінця файлу за вказівником файлу

### Опис

```methodsynopsis
public streamWrapper::stream_eof(): bool
```

Цей метод викликається в результаті виклику [feof()](function.feof.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повинен повернути **`true`**якщо позиція читання/запису знаходиться в кінці потоку і доступних для читання даних більше немає. В інших випадках повертається **`false`**

### Примітки

**Увага**

При читанні файлу повністю (наприклад, функцією [file\_get\_contents()](function.file-get-contents.html)), PHP буде викликати [streamWrapper::stream\_read()](streamwrapper.stream-read.html) і разом із ним **streamWrapper::streameof()** у циклі, поки [streamWrapper::stream\_read()](streamwrapper.stream-read.html) повертає непустий рядок. Повертається з **streamWrapper::streameof()** значення у своїй ігнорується.

### Дивіться також

-   [feof()](function.feof.html) - Перевіряє, чи кінець файлу досягнуто