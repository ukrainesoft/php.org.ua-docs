Вибирає всі значення масиву

-   [« array\_unshift](function.array-unshift.html)
    
-   [array\_walk\_recursive »](function.array-walk-recursive.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
-   Вибирає всі значення масиву
    

# arrayvalues

(PHP 4, PHP 5, PHP 7, PHP 8)

arrayvalues ​​- Вибирає всі значення масиву

### Опис

```methodsynopsis
array_values(array $array): array
```

**arrayvalues()** повертає масив з усіма елементами масиву `array`. Вона також заново індексує масив, що повертається, числовими індексами.

### Список параметрів

`array`

Масив.

### Значення, що повертаються

Повертає індексований масив значень.

### Приклади

**Приклад #1 Приклад використання **arrayvalues()****

```php
<?php
$array = array("size" => "XL", "color" => "gold");
print_r(array_values($array));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => XL
    [1] => gold
)
```

### Дивіться також

-   [array\_keys()](function.array-keys.html) - Повертає все або деяке підмножина ключів масиву
-   [array\_combine()](function.array-combine.html) - Створює новий масив, використовуючи один масив як ключі, а інший для його значень