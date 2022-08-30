Отримати список зареєстрованих фільтрів

-   [« streamgetcontents](function.stream-get-contents.html)
    
-   [streamgetline »](function.stream-get-line.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з потоками](ref.stream.html)
    
-   Отримати список зареєстрованих фільтрів
    

# streamgetfilters

(PHP 5, PHP 7, PHP 8)

streamgetfilters — Отримати список зареєстрованих фільтрів

### Опис

```methodsynopsis
stream_get_filters(): array
```

Отримати список зареєстрованих фільтрів у запущеній системі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає індексований масив, що містить найменування всіх доступних системних фільтрів потоку.

### Приклади

**Приклад #1 Приклад використання функції **streamgetfilters()****

```php
<?php
$streamlist = stream_get_filters();
print_r($streamlist);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array (
  [0] => string.rot13
  [1] => string.toupper
  [2] => string.tolower
  [3] => string.base64
  [4] => string.quoted-printable
)
```

### Дивіться також

-   [streamfilterregister()](function.stream-filter-register.html) - Реєструє потоковий фільтр, визначений користувачем
-   [streamgetwrappers()](function.stream-get-wrappers.html) - Отримати список зареєстрованих потоків