Обчислює суму значень масиву

-   [« arraysplice](function.array-splice.html)
    
-   [arrayudiffassoc »](function.array-udiff-assoc.html)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи з масивами](ref.array.md)
    
-   Обчислює суму значень масиву
    

# arraysum

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

arraysum - Обчислює суму значень масиву

### Опис

```methodsynopsis
array_sum(array $array): int|float
```

**arraysum()** повертає суму значень масиву.

### Список параметрів

`array`

Вхідний масив

### Значення, що повертаються

Повертає суму значень у вигляді цілого числа чи числа з плаваючою точкою; `0`, якщо `array` порожній.

### Приклади

**Приклад #1 Приклад використання **arraysum()****

```php
<?php
$a = array(2, 4, 6, 8);
echo "sum(a) = " . array_sum($a) . "\n";

$b = array("a" => 1.2, "b" => 2.3, "c" => 3.4);
echo "sum(b) = " . array_sum($b) . "\n";
?>
```

Результат виконання цього прикладу:

```
sum(a) = 20
sum(b) = 6.9
```