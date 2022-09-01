---
navigation:
  - ds-sequence.apply.html: '« DsSequence::apply'
  - ds-sequence.contains.html: 'ДсSequence::contains »'
  - index.html: PHP Manual
  - class.ds-sequence.html: Послідовність
title: 'ДсSequence::capacity'
---
# ДсSequence::capacity

(PECL ds >= 1.0.0)

ДсSequence::capacity — Повертає поточну місткість

### Опис

```methodsynopsis
abstract public Ds\Sequence::capacity(): int
```

Повертає поточну місткість.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна місткість.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::capacity()****

```php
<?php
$sequence = new \Ds\Vector();
var_dump($sequence->capacity());

$sequence->push(...range(1, 50));
var_dump($sequence->capacity());

$sequence[] = "a";
var_dump($sequence->capacity());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(10)
int(50)
int(75)
```
