Обчислити добуток значень масиву

-   [« array\_pop](function.array-pop.html)
    
-   [array\_push »](function.array-push.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
-   Обчислити добуток значень масиву
    

# arrayproduct

(PHP 5> = 5.1.0, PHP 7, PHP 8)

arrayproduct — Обчислити добуток значень масиву

### Опис

```methodsynopsis
array_product(array $array): int|float
```

**arrayproduct()** повертає добуток значень масиву.

### Список параметрів

`array`

Масив.

### Значення, що повертаються

Повертає твір як тип integer чи float.

### Приклади

**Приклад #1 Приклади використання **arrayproduct()****

```php
<?php

$a = array(2, 4, 6, 8);
echo "product(a) = " . array_product($a) . "\n";
echo "product(array()) = " . array_product(array()) . "\n";

?>
```

Результат виконання цього прикладу:

```
product(a) = 384
product(array()) = 1
```