Закриває ресурс

-   [« streamWrapper::stream\_cast](streamwrapper.stream-cast.html)
    
-   [streamWrapper::stream\_eof »](streamwrapper.stream-eof.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Закриває ресурс
    

# streamWrapper::streamclose

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::streamclose — Закриває ресурс

### Опис

```methodsynopsis
public streamWrapper::stream_close(): void
```

Цей метод викликається у процесі виконання [fclose()](function.fclose.html)

Усі ресурси, виділені або заблоковані обгорткою, мають бути звільнені.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [fclose()](function.fclose.html) - Закриває відкритий дескриптор файлу
-   [streamWrapper::dir\_closedir()](streamwrapper.dir-closedir.html) - Закрити дескриптор директорії