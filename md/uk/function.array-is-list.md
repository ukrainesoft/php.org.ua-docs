---
navigation:
  - function.array-intersect.md: « arrayintersect
  - function.array-key-exists.md: arraykeyexists »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayісlist
---
# arrayісlist

(PHP 8> = 8.1.0)

arrayісlist — Перевіряє, чи є цей `array` списком

### Опис

```methodsynopsis
array_is_list(array $array): bool
```

Визначає, чи є даний `array` списком. Масив (array) вважається списком, якщо його ключі складаються з послідовних чисел від `0` до `count($array)-1`

### Список параметрів

`array`

Масив (Array) для перевірки.

### Значення, що повертаються

Повертає **`true`**, якщо `array` є списком, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **arrayісlist()****

```php
<?php

array_is_list([]); // true
array_is_list(['apple', 2, 3]); // true
array_is_list([0 => 'apple', 'orange']); // true

// Масив начинается не с 0
array_is_list([1 => 'apple', 'orange']); // false

// Ключи Масива не по порядку
array_is_list([1 => 'apple', 0 => 'orange']); // false

// Ключи Масива не являются целыми числами
array_is_list([0 => 'apple', 'foo' => 'bar']); // false

// Непоследовательные ключи
array_is_list([0 => 'apple', 2 => 'bar']); // false
?>
```

### Примітки

> **Зауваження**
> 
> Функція повертає **`true`** для пустих масивів.

### Дивіться також

-   [arrayvalues()](function.array-values.md) - Вибирає всі значення масиву
