Закриває ресурс

-   [« streamWrapper::streamcast](streamwrapper.stream-cast.html)
    
-   [streamWrapper::streameof »](streamwrapper.stream-eof.html)
    
-   [PHP Manual](index.md)
    
-   [streamWrapper](class.streamwrapper.md)
    
-   Закриває ресурс
    

# streamWrapper::streamclose

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::streamclose — Закриває ресурс

### Опис

```methodsynopsis
public streamWrapper::stream_close(): void
```

Цей метод викликається у процесі виконання [fclose()](function.fclose.md)

Усі ресурси, виділені або заблоковані обгорткою, мають бути звільнені.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [fclose()](function.fclose.md) - Закриває відкритий дескриптор файлу
-   [streamWrapper::dirclosedir()](streamwrapper.dir-closedir.html) - Закрити дескриптор директорії