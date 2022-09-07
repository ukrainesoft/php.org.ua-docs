---
navigation:
  - ds-sequence.pop.md: '« DsSequence::pop'
  - ds-sequence.reduce.md: 'ДсSequence::reduce »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Послідовність
title: 'ДсSequence::push'
---
# ДсSequence::push

(PECL ds >= 1.0.0)

ДсSequence::push — Додає значення до кінця послідовності

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

**Приклад #1 Приклад використання **ДсSequence::push()****

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

Результатом виконання цього прикладу буде щось подібне:

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
