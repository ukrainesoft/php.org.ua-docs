---
navigation:
  - ds-vector.slice.md: '« Ds\\Vector::slice'
  - ds-vector.sorted.md: 'Ds\\Vector::sorted »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::sort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::sort

(PECL ds >= 1.0.0)

Ds\\Vector::sort — Сортує вектор

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

Возвращение*нецілих* значень з функції порівняння, таких як число з плаваючою точкою (float), призведе до внутрішнього приведення значення callback-функції, що повертається, до цілого числа (int). Таким чином, значення `0.99`и`0.1` будуть приведені до цілого значення що дозволить порівняти ці значення як рівні.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\Vector::sort()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector([4, 5, 1, 3, 2]);
$vector->sort();

print_r($vector);
?>
```

Висновок наведеного прикладу буде схожим на:

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

**Приклад #2 Приклад використання** Ds\\Vector::sort()\*\* з callback-функцією порівняння\*\*

```php
<?php
$vector = new \Ds\Vector([4, 5, 1, 3, 2]);

$vector->sort(function($a, $b) {
    return $b <=> $a;
});

print_r($vector);
?>
```

Висновок наведеного прикладу буде схожим на:

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
