Перетворити повне ім'я файлу, використовуючи шляхи включення

-   [« streamregisterwrapper](function.stream-register-wrapper.html)
    
-   [streamselect »](function.stream-select.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з потоками](ref.stream.html)
    
-   Перетворити повне ім'я файлу, використовуючи шляхи включення
    

# streamresolveincludepath

(PHP 5> = 5.3.2, PHP 7, PHP 8)

streamresolveincludepath — Перетворити повне ім'я файлу за допомогою шляхів увімкнення.

### Опис

```methodsynopsis
stream_resolve_include_path(string $filename): string|false
```

Перетворити повне ім'я файлу з параметра `filename`, використовуючи шляхи включення відповідно до тих же правил, що і функції [fopen()](function.fopen.html)[include](function.include.html)

### Список параметрів

`filename`

Ім'я файлу, яке потрібно перетворити.

### Значення, що повертаються

Повертає рядок (string), що містить отримане абсолютне ім'я файлу або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **streamresolveincludepath()****

Основний приклад використання.

```php
<?php
var_dump(stream_resolve_include_path("test.php"));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(22) "/var/www/html/test.php"
```