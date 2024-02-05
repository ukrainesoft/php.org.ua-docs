---
navigation:
  - ds-sequence.pop.md: '« Ds\\Sequence::pop'
  - ds-sequence.reduce.md: 'Ds\\Sequence::reduce »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::push'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::push

(PECL ds >= 1.0.0)

Ds\\Sequence::push — Додає значення до кінця послідовності

### Опис

```methodsynopsis
abstract public Ds\Sequence::push(mixed ...$values): void
```

Додає значення до кінця послідовності.

### Список параметрів

`values`

Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\Sequence::push()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector();

$sequence->push("a");
$sequence->push("b");
$sequence->push("c", "d");
$sequence->push(...["e", "f"]);

print_r($sequence);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Vector Object
(
    [0] => a
    [1] => b
    [2] => c
    [3] => d
    [4] => e
    [5] => f
)
```
