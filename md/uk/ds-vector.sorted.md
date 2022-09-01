---
navigation:
  - ds-vector.sort.html: '« DsVector::sort'
  - ds-vector.sum.html: 'ДсVector::sum »'
  - index.md: PHP Manual
  - class.ds-vector.html: Вектор
title: 'ДсVector::sorted'
---
# ДсVector::sorted

(PECL ds >= 1.0.0)

ДсVector::sorted — Повертає копію колекції, відсортовану за значенням.

### Опис

```methodsynopsis
public Ds\Vector::sorted(callable $comparator = ?): Ds\Vector
```

Повертає відсортовану копію колекції, опціонально використовуючи callback-функцію `comparator`

### Список параметрів

`comparator`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

**Застереження**

*Не ціле* значення, повернене з функції порівняння, такого як float, буде приведено до цілої кількості (int). Отже значення типу 0.99 і 0.1 будуть наведені до 0, що означатиме рівність порівнюваних значень.

### Значення, що повертаються

Повертає копію колекції, відсортовану за значенням.

### Приклади

**Приклад #1 Приклад використання **ДсVector::sorted()****

```php
<?php
$vector = new \Ds\Vector([4, 5, 1, 3, 2]);

print_r($vector->sorted());
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

**Приклад #2 Приклад використання **ДсVector::sorted()** з callback-функцією порівняння**

```php
<?php
$vector = new \Ds\Vector([4, 5, 1, 3, 2]);

$sorted = $vector->sorted(function($a, $b) {
    return $b <=> $a;
});

print_r($sorted);
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
