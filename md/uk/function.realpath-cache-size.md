Отримує розмір кеша realpath

-   [« realpathcacheget](function.realpath-cache-get.html)
    
-   [realpath »](function.realpath.html)
    
-   [PHP Manual](index.html)
    
-   [Функції файлової системи](ref.filesystem.html)
    
-   Отримує розмір кеша realpath
    

# realpathcachesize

(PHP 5> = 5.3.2, PHP 7, PHP 8)

realpathcachesize — Отримує розмір кеша realpath

### Опис

```methodsynopsis
realpath_cache_size(): int
```

Отримує обсяг пам'яті, який використовується кешем realpath.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає скільки використовується кеш-пам'яті realpath.

### Приклади

**Приклад #1 Приклад використання **realpathcachesize()****

```php
<?php
var_dump(realpath_cache_size());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(412)
```

### Дивіться також

-   [realpathcacheget()](function.realpath-cache-get.html) - Отримує записи з кеша realpath
-   Конфігураційна опція [realpathcachesize](ini.core.html#ini.realpath-cache-size)