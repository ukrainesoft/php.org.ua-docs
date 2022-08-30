Зупиняє профіль xhprof

-   [« Функции Xhprof](ref.xhprof.html)
    
-   [xhprofenable »](function.xhprof-enable.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Xhprof](ref.xhprof.html)
    
-   Зупиняє профіль xhprof
    

# xhprofdisable

(PECL xhprof >= 0.9.0)

xhprofdisable — Зупиняє профіль xhprof

### Опис

```methodsynopsis
xhprof_disable(): array
```

Зупиняє профіль та повертає зібрані дані.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив із результатами профілювання.

### Приклади

**Приклад #1 Приклад використання **xhprofdisable()****

```php
<?php
xhprof_enable();

$foo = strlen("foo bar");

$xhprof_data = xhprof_disable();

print_r($xhprof_data);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [main()==>strlen] => Array
        (
            [ct] => 1
            [wt] => 279
        )

    [main()==>xhprof_disable] => Array
        (
            [ct] => 1
            [wt] => 9
        )

    [main()] => Array
        (
            [ct] => 1
            [wt] => 610
        )

)
```