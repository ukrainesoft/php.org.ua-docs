---
navigation:
  - ds-vector.slice.md: '« DsVector::slice'
  - ds-vector.sorted.md: 'ДсVector::sorted »'
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::sort'
---
# ДсVector::sort

(PECL ds >= 1.0.0)

ДсVector::sort — Сортує вектор

### Опис

```methodsynopsis
public Ds\Vector::sort(callable $comparator = ?): void
```

Сортує вектор, опціонально використовуючи callback-функцію `comparator`

### Список параметрів

`comparator`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

**Застереження**

*Не ціле* значення, повернене з функції порівняння, такого як float, буде приведено до цілої кількості (int). Отже значення типу 0.99 і 0.1 будуть наведені до 0, що означатиме рівність порівнюваних значень.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсVector::sort()****

```php
<?php
$vector = new \Ds\Vector([4, 5, 1, 3, 2]);
$vector->sort();

print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
)
```

**Приклад #2 Приклад використання **ДсVector::sort()** з callback-функцією порівняння**

```php
<?php
$vector = new \Ds\Vector([4, 5, 1, 3, 2]);

$vector->sort(function($a, $b) {
    return $b <=> $a;
});

print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => 5
    [1] => 4
    [2] => 3
    [3] => 2
    [4] => 1
)
```
