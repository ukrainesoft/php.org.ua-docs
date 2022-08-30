Перевіряє досягнення кінця файлу за файловим покажчиком

-   [« streamWrapper::streamclose](streamwrapper.stream-close.html)
    
-   [streamWrapper::streamflush »](streamwrapper.stream-flush.html)
    
-   [PHP Manual](index.md)
    
-   [streamWrapper](class.streamwrapper.md)
    
-   Перевіряє досягнення кінця файлу за файловим покажчиком
    

# streamWrapper::streameof

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::streameof — Перевіряє досягнення кінця файлу за вказівником файлу

### Опис

```methodsynopsis
public streamWrapper::stream_eof(): bool
```

Цей метод викликається в результаті виклику [feof()](function.feof.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повинен повернути \*\*`true`\*\*якщо позиція читання/запису знаходиться в кінці потоку і доступних для читання даних більше немає. В інших випадках повертається **`false`**

### Примітки

**Увага**

При читанні файлу повністю (наприклад, функцією [filegetcontents()](function.file-get-contents.html)), PHP буде викликати [streamWrapper::streamread()](streamwrapper.stream-read.html) і разом із ним **streamWrapper::streameof()** у циклі, поки [streamWrapper::streamread()](streamwrapper.stream-read.html) повертає непустий рядок. Повертається з **streamWrapper::streameof()** значення у своїй ігнорується.

### Дивіться також

-   [feof()](function.feof.md) - Перевіряє, чи кінець файлу досягнуто