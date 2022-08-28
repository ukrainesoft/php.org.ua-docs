Отримати список зареєстрованих потоків

-   [« stream\_get\_transports](function.stream-get-transports.html)
    
-   [stream\_is\_local »](function.stream-is-local.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Отримати список зареєстрованих потоків
    

# streamgetwrappers

(PHP 5, PHP 7, PHP 8)

streamgetwrappers — Отримати список зареєстрованих потоків

### Опис

```methodsynopsis
stream_get_wrappers(): array
```

Витягує список зареєстрованих потоків на запущеній системі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає індексований масив, що містить назви всіх обертів потоків, доступних на запущеній системі.

### Приклади

**Приклад #1 Приклад використання **streamgetwrappers()****

```php
<?php
print_r(stream_get_wrappers());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => php
    [1] => file
    [2] => http
    [3] => ftp
    [4] => compress.bzip2
    [5] => compress.zlib
)
```

**Приклад #2 Перевірка існування обгортки потоку**

```php
<?php
// Проверяет существование обёртки потока bzip2
if (in_array('compress.bzip2', stream_get_wrappers())) {
    echo 'compress.bzip2:// поддержка включена.';
} else {
    echo 'compress.bzip2:// поддержка не включена.';
}
?>
```

### Дивіться також

-   [stream\_wrapper\_register()](function.stream-wrapper-register.html) - реєструє обгортку URL, реалізовану у вигляді PHP-класу