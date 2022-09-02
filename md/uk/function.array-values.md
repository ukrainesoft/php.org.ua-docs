---
navigation:
  - function.array-unshift.md: « arrayunshift
  - function.array-walk-recursive.md: arraywalkrecursive »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayvalues
---
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

-   [arraykeys()](function.array-keys.md) - Повертає все або деяке підмножина ключів масиву
-   [arraycombine()](function.array-combine.md) - Створює новий масив, використовуючи один масив як ключі, а інший для його значень
