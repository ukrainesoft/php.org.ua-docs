Повертає масив імен усіх скомпілованих та завантажених модулів

-   [« get\_included\_files](function.get-included-files.html)
    
-   [get\_magic\_quotes\_gpc »](function.get-magic-quotes-gpc.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
-   Повертає масив імен усіх скомпілованих та завантажених модулів
    

# getloadedextensions

(PHP 4, PHP 5, PHP 7, PHP 8)

getloadedextensions — Повертає масив імен усіх скомпілованих та завантажених модулів

### Опис

```methodsynopsis
get_loaded_extensions(bool $zend_extensions = false): array
```

Функція повертає масив імен усіх скомпільованих та завантажених в інтерпретаторі PHP модулів.

### Список параметрів

`zend_extensions`

Повернути тільки модулі Zend або звичайні модулі, такі як mysqli. За замовчуванням **`false`** (Повернення звичайних модулів).

### Значення, що повертаються

Повертає індексований масив імен усіх модулів.

### Приклади

**Приклад #1 Приклад використання **getloadedextensions()****

```php
<?php
print_r(get_loaded_extensions());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
   [0] => xml
   [1] => wddx
   [2] => standard
   [3] => session
   [4] => posix
   [5] => pgsql
   [6] => pcre
   [7] => gd
   [8] => ftp
   [9] => db
   [10] => calendar
   [11] => bcmath
)
```

### Дивіться також

-   [get\_extension\_funcs()](function.get-extension-funcs.html) - Повертає масив імен функцій модуля
-   [extension\_loaded()](function.extension-loaded.html) - Визначає, чи завантажений модуль
-   [dl()](function.dl.html) - Завантажує модуль PHP під час виконання
-   [phpinfo()](function.phpinfo.html) - Виводить інформацію про поточну конфігурацію PHP