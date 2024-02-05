---
navigation:
  - ds-sequence.sum.md: '« Ds\\Sequence::sum'
  - class.ds-vector.md: Ds\\Vector »
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::unshift'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::unshift

(PECL ds >= 1.0.0)

Ds\\Sequence::unshift — Додає значення на початок послідовності

### Опис

```methodsynopsis
abstract public Ds\Sequence::unshift(mixed $values = ?): void
```

Додає значення на початок послідовності, переміщуючи всі поточні значення вперед, щоб звільнити місце для нових значень.

### Список параметрів

`values`

Значення, що додаються.

> **Зауваження** :
> 
> Багато значень додаються в тому порядку, як вони були передані.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\Sequence::unshift()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

$sequence->unshift("a");
$sequence->unshift("b", "c");

print_r($sequence);
?>
```

Висновок наведеного прикладу буде схожим на:

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
