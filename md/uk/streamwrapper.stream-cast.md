Отримує ресурс рівнем нижче

-   [« streamWrapper::rmdir](streamwrapper.rmdir.md)
    
-   [streamWrapper::streamclose »](streamwrapper.stream-close.html)
    
-   [PHP Manual](index.md)
    
-   [streamWrapper](class.streamwrapper.md)
    
-   Отримує ресурс рівнем нижче
    

# streamWrapper::streamcast

(PHP 5> = 5.3.0, PHP 7, PHP 8)

streamWrapper::streamcast — Отримує ресурс рівнем нижче

### Опис

```methodsynopsis
public streamWrapper::stream_cast(int $cast_as): resource
```

Цей метод викликається у процесі виконання [streamselect()](function.stream-select.html)

### Список параметрів

`cast_as`

Може бути **`STREAM_CAST_FOR_SELECT`**, коли [streamselect()](function.stream-select.html) викликає **streamcast()**, або **`STREAM_CAST_AS_STREAM`**, коли **streamcast()** викликається задля інших цілей.

### Значення, що повертаються

Повинен повернути ресурс потоку, що лежить рівнем нижче, або **`false`**

### Дивіться також

-   [streamselect()](function.stream-select.html) - Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds