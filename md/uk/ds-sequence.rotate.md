---
navigation:
  - ds-sequence.reversed.md: '« Ds\\Sequence::reversed'
  - ds-sequence.set.md: 'Ds\\Sequence::set »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::rotate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::rotate

(PECL ds >= 1.0.0)

Ds\\Sequence::rotate — Перемотує послідовність на задану кількість значень

### Опис

```methodsynopsis
abstract public Ds\Sequence::rotate(int $rotations): void
```

Перемотує послідовність на задану кількість значень. Ця операція аналогічна до виконання заданої кількості разів коду `$sequence->push($sequence->shift())`якщо кількість оборотів позитивно і `$sequence->unshift($sequence->pop())`якщо негативно.

### Список параметрів

`rotations`

Кількість значень, які треба "перемотати".

### Значення, що повертаються

Функція не повертає значення після виконання. Буде змінено поточну послідовність.

### Приклади

**Приклад #1 Приклад використання** Ds\\Sequence::rotate()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c", "d"]);

$sequence->rotate(1);  // Аналогично $a = $sequence->shift(); $sequence->push($a);
print_r($sequence);

$sequence->rotate(2);
print_r($sequence);
?>
```

Висновок наведеного прикладу буде схожим на:

```
(
    [0] => b
    [1] => c
    [2] => d
    [3] => a
)
Ds\Vector Object
(
    [0] => d
    [1] => a
    [2] => b
    [3] => c
)
```
