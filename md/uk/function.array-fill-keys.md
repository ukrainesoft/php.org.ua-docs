---
navigation:
  - function.array-diff.md: « array\_diff
  - function.array-fill.md: array\_fill »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_fill\_keys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_fill\_keys

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

array\_fill\_keys — Створює масив та заповнює його значеннями з певними ключами

### Опис

```methodsynopsis
array_fill_keys(array $keys, mixed $value): array
```

Створює та заповнює масив значенням параметра `value`, используя значения массива`keys` як ключі.

### Список параметрів

`keys`

Масив значень, які будуть використані як ключі. Некоректні ключі масиву будуть перетворені на рядок (string).

`value`

Заповнюване значення

### Значення, що повертаються

Повертає заповнений масив

### Приклади

**Приклад #1 Приклад використання** array\_fill\_keys()\*\*\*\*

```php
<?php
$keys = array('foo', 5, 10, 'bar');
$a = array_fill_keys($keys, 'banana');
print_r($a);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [foo] => banana
    [5] => banana
    [10] => banana
    [bar] => banana
)
```

### Дивіться також

-   [array\_fill()](function.array-fill.md) \- Заповнює масив значеннями
-   [array\_combine()](function.array-combine.md) \- Створює новий масив, використовуючи один масив як ключі, а інший для його значень
