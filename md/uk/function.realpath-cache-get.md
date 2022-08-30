Отримує записи з кеша realpath

-   [« readlink](function.readlink.html)
    
-   [realpathcachesize »](function.realpath-cache-size.html)
    
-   [PHP Manual](index.html)
    
-   [Функції файлової системи](ref.filesystem.html)
    
-   Отримує записи з кеша realpath
    

# realpathcacheget

(PHP 5> = 5.3.2, PHP 7, PHP 8)

realpathcacheget — Отримує записи з кеша realpath

### Опис

```methodsynopsis
realpath_cache_get(): array
```

Отримує вміст кешу реального шляху.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив записів із кеша realpath. Ключі є записами realpath, а значення є масивами даних, що містять обчислений шлях, час життя кеша та інших даних, що зберігаються у кеші.

### Приклади

**Приклад #1 Приклад використання **realpathcacheget()****

```php
<?php
var_dump(realpath_cache_get());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {
  ["/test"] => array(4) {
    ["key"] => int(123456789)
    ["is_dir"] => bool(true)
    ["realpath"] => string(5) "/test"
    ["expires"] => int(1260318939)
  }
  ["/test/test.php"] => array(4) {
    ["key"] => int(987654321)
    ["is_dir"] => bool(false)
    ["realpath"] => string(12) "/root/test.php"
    ["expires"] => int(1260318939)
  }
}
```

### Дивіться також

-   [realpathcachesize()](function.realpath-cache-size.html) - Отримує розмір кеша realpath