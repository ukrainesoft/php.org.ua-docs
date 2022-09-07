---
navigation:
  - ds-sequence.sum.md: '« DsSequence::sum'
  - class.ds-vector.md: Вектор »
  - index.md: PHP Manual
  - class.ds-sequence.md: Послідовність
title: 'ДсSequence::unshift'
---
# ДсSequence::unshift

(PECL ds >= 1.0.0)

ДсSequence::unshift — Додає значення на початок послідовності

### Опис

```methodsynopsis
abstract public Ds\Sequence::unshift(mixed $values = ?): void
```

Додає значення на початок послідовності, переміщуючи всі поточні значення вперед, щоб звільнити місце для нових значень.

### Список параметрів

`values`

Значення, що додаються.

> **Зауваження**
> 
> Багато значень додаються в тому порядку, як вони були передані.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::unshift()****

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

$sequence->unshift("a");
$sequence->unshift("b", "c");

print_r($sequence);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => b
    [1] => c
    [2] => a
    [3] => 1
    [4] => 2
    [5] => 3
)
```
