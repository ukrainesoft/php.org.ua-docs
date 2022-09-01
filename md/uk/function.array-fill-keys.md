---
navigation:
  - function.array-diff.html: « arraydiff
  - function.array-fill.html: arrayfill »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayfillkeys
---
# arrayfillkeys

(PHP 5> = 5.2.0, PHP 7, PHP 8)

arrayfillkeys — Створює масив та заповнює його значеннями з певними ключами

### Опис

```methodsynopsis
array_fill_keys(array $keys, mixed $value): array
```

Створює та заповнює масив значенням параметра `value`, використовуючи значення масиву `keys` як ключі.

### Список параметрів

`keys`

Масив значень, які будуть використані як ключі. Некоректні ключі масиву будуть перетворені на рядок (string).

`value`

Заповнюване значення

### Значення, що повертаються

Повертає заповнений масив

### Приклади

**Приклад #1 Приклад використання **arrayfillkeys()****

```php
<?php
$keys = array('foo', 5, 10, 'bar');
$a = array_fill_keys($keys, 'banana');
print_r($a);
?>
```

Результат виконання цього прикладу:

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

-   [arrayfill()](function.array-fill.md) - Заповнює масив значеннями
-   [arraycombine()](function.array-combine.md) - Створює новий масив, використовуючи один масив як ключі, а інший для його значень
