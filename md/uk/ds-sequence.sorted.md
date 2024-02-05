---
navigation:
  - ds-sequence.sort.md: '« Ds\\Sequence::sort'
  - ds-sequence.sum.md: 'Ds\\Sequence::sum »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::sorted'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::sorted

(PECL ds >= 1.0.0)

Ds\\Sequence::sorted — Повертає копію колекції, відсортовану за значенням.

### Опис

```methodsynopsis
abstract public Ds\Sequence::sorted(callable $comparator = ?): Ds\Sequence
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

**Пример #1 Пример использования**Ds\\Sequence::sorted()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector([4, 5, 1, 3, 2]);

print_r($sequence->sorted());
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

**Пример #2 Пример использования**Ds\\Sequence::sorted()\*\* з callback-функцією порівняння\*\*

```php
<?php
$sequence = new \Ds\Vector([4, 5, 1, 3, 2]);

$sorted = $sequence->sorted(function($a, $b) {
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
