Отримує ресурс рівнем нижче

-   [« streamWrapper::rmdir](streamwrapper.rmdir.html)
    
-   [streamWrapper::stream\_close »](streamwrapper.stream-close.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Отримує ресурс рівнем нижче
    

# streamWrapper::streamcast

(PHP 5> = 5.3.0, PHP 7, PHP 8)

streamWrapper::streamcast — Отримує ресурс рівнем нижче

### Опис

```methodsynopsis
public streamWrapper::stream_cast(int $cast_as): resource
```

Цей метод викликається у процесі виконання [stream\_select()](function.stream-select.html)

### Список параметрів

`cast_as`

Може бути **`STREAM_CAST_FOR_SELECT`**, коли [stream\_select()](function.stream-select.html) викликає **streamcast()**, або **`STREAM_CAST_AS_STREAM`**, коли **streamcast()** викликається задля інших цілей.

### Значення, що повертаються

Повинен повернути ресурс потоку, що лежить рівнем нижче, або **`false`**

### Дивіться також

-   [stream\_select()](function.stream-select.html) - Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds