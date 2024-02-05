---
navigation:
  - function.array-intersect.md: « array\_intersect
  - function.array-key-exists.md: array\_key\_exists »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_is\_list
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_is\_list

(PHP 8 >= 8.1.0)

array\_is\_list — Перевіряє, чи є цей `array`списком

### Опис

```methodsynopsis
array_is_list(array $array): bool
```

Визначає, чи є даний `array` списком. Масив (array) вважається списком, якщо його ключі складаються з послідовних чисел від до`count($array)-1`

### Список параметрів

`array`

Масив (Array) для перевірки.

### Значення, що повертаються

Повертає **`true`**, якщо `array` є списком, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання** array\_is\_list()\*\*\*\*

```php
<?php

array_is_list([]); // true
array_is_list(['apple', 2, 3]); // true
array_is_list([0 => 'apple', 'orange']); // true

// Массив начинается не с 0
array_is_list([1 => 'apple', 'orange']); // false

// Ключи массива не по порядку
array_is_list([1 => 'apple', 0 => 'orange']); // false

// Ключи массива не являются целыми числами
array_is_list([0 => 'apple', 'foo' => 'bar']); // false

// Непоследовательные ключи
array_is_list([0 => 'apple', 2 => 'bar']); // false
?>
```

### Примітки

> **Зауваження** :
> 
> Функція повертає **`true`** для пустих масивів.

### Дивіться також

-   [array\_values()](function.array-values.md) \- Повертає всі значення масиву
