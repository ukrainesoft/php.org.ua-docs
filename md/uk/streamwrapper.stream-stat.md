Отримання інформації про файловий ресурс

-   [« streamWrapper::stream\_set\_option](streamwrapper.stream-set-option.html)
    
-   [streamWrapper::stream\_tell »](streamwrapper.stream-tell.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Отримання інформації про файловий ресурс
    

# streamWrapper::streamстати

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::streamstat — Отримання інформації про файловий ресурс

### Опис

```methodsynopsis
public streamWrapper::stream_stat(): array|false
```

Цей метод викликається внаслідок виклику функції [fstat()](function.fstat.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Дивіться [stat()](function.stat.html)

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Дивіться також

-   [stat()](function.stat.html) - Повертає інформацію про файл
-   [streamwrapper::url\_stat()](streamwrapper.url-stat.html) - Отримання інформації про файл