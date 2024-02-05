---
navigation:
  - ds-vector.sort.md: '« Ds\\Vector::sort'
  - ds-vector.sum.md: 'Ds\\Vector::sum »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::sorted'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::sorted

(PECL ds >= 1.0.0)

Ds\\Vector::sorted — Повертає копію колекції, відсортовану за значенням.

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

Возвращение*нецілих* значень з функції порівняння, таких як число з плаваючою точкою (float), призведе до внутрішнього приведення значення callback-функції, що повертається, до цілого числа (int). Таким чином, значення `0.99`и`0.1` будуть приведені до цілого значення що дозволить порівняти ці значення як рівні.

### Значення, що повертаються

Повертає копію колекції, відсортовану за значенням.

### Приклади

**Приклад #1 Приклад використання** Ds\\Vector::sorted()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector([4, 5, 1, 3, 2]);

print_r($vector->sorted());
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

**Приклад #2 Приклад використання** Ds\\Vector::sorted()\*\* з callback-функцією порівняння\*\*

```php
<?php
$vector = new \Ds\Vector([4, 5, 1, 3, 2]);

$sorted = $vector->sorted(function($a, $b) {
    return $b <=> $a;
});

print_r($sorted);
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
