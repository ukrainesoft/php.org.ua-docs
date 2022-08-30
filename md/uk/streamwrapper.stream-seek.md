Переміщення на задану позицію у потоці

-   [« streamWrapper::streamread](streamwrapper.stream-read.html)
    
-   [streamWrapper::streamsetoption »](streamwrapper.stream-set-option.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Переміщення на задану позицію у потоці
    

# streamWrapper::streamseek

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::streamseek — Переміщення на задану позицію у потоці

### Опис

```methodsynopsis
public streamWrapper::stream_seek(int $offset, int $whence  = SEEK_SET): bool
```

Цей метод викликається у процесі виконання [fseek()](function.fseek.html)

Позицію читання/запису в потоці необхідно оновлювати відповідно до аргументів `offset` і `whence`

### Список параметрів

`offset`

Зміщення у потоці, на яке потрібно переміститися.

`whence`

Можливі значення:

-   **`SEEK_SET`** - Переміститися на позицію `offset` байт з початку файла.
-   **`SEEK_CUR`** - Переміститися на `offset` байт щодо поточної позиції.
-   **`SEEK_END`** - Переміститися на позицію `offset` байт від кінця файлу.

> **Зауваження**: Поточна реалізація ніколи не встановлює для `whence` значення **`SEEK_CUR`**; натомість такі пошуки внутрішньо перетворюються на пошуки **`SEEK_SET`**

### Значення, що повертаються

Повертає **`true`**, якщо позиція оновлена, **`false`** в інших випадках.

### Примітки

> **Зауваження**
> 
> Якщо не реалізований, як значення, що повертається, приймається **`false`**

> **Зауваження**
> 
> У разі успішного виконання [streamWrapper::streamtell()](streamwrapper.stream-tell.html) буде викликано відразу після того, як **streamWrapper::streamseek()** відпрацює. Якщо виконання [streamWrapper::streamtell()](streamwrapper.stream-tell.html) завершиться невдачею, то викликаючу функцію буде повернуто значення **`false`**

> **Зауваження**
> 
> Не всі операції переміщення у потоці призведуть до виклику цієї функції. У PHP за замовчуванням включена буферизація потоків (дивіться також [streamsetreadbuffer()](function.stream-set-read-buffer.html)), тому переміщення в потоці може означати лише переміщення покажчика буфері.

### Дивіться також

-   [fseek()](function.fseek.html) - Встановлює зміщення у файловому покажчику