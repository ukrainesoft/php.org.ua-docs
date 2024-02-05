---
navigation:
  - function.array-unshift.md: « array\_unshift
  - function.array-walk-recursive.md: array\_walk\_recursive »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_values
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_values

(PHP 4, PHP 5, PHP 7, PHP 8)

array\_values ​​— Повертає всі значення масиву

### Опис

```methodsynopsis
array_values(array $array): array
```

Функция**array\_values()** повертає індексний масив з усіма значеннями масиву `array`

### Список параметрів

`array`

Масив.

### Значення, що повертаються

Повертає індексний масив значень.

### Приклади

**Пример #1 Пример использования функции**array\_values()\*\*\*\*

```php
<?php

$array = array("size" => "XL", "color" => "gold");
print_r(array_values($array));
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => XL
    [1] => gold
)
```

### Дивіться також

-   [array\_keys()](function.array-keys.md) \- Повертає все або деяке підмножина ключів масиву
-   [array\_combine()](function.array-combine.md) \- Створює новий масив, використовуючи один масив як ключі, а інший для його значень
