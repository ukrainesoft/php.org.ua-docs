---
navigation:
  - ds-sequence.remove.md: '« DsSequence::remove'
  - ds-sequence.reversed.md: 'ДсSequence::reversed »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Послідовність
title: 'ДсSequence::reverse'
---
# ДсSequence::reverse

(PECL ds >= 1.0.0)

ДсSequence::reverse — Перевертає поточну колекцію

### Опис

```methodsynopsis
abstract public Ds\Sequence::reverse(): void
```

Перевертає поточну колекцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::reverse()****

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);
$sequence->reverse();

print_r($sequence);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => c
    [1] => b
    [2] => a
)
```
