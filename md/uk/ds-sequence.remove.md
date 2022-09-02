---
navigation:
  - ds-sequence.reduce.md: '« DsSequence::reduce'
  - ds-sequence.reverse.md: 'ДсSequence::reverse »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Послідовність
title: 'ДсSequence::remove'
---
# ДсSequence::remove

(PECL ds >= 1.0.0)

ДсSequence::remove — Видаляє та повертає значення за індексом

### Опис

```methodsynopsis
abstract public Ds\Sequence::remove(int $index): mixed
```

Видаляє та повертає значення за індексом.

### Список параметрів

`index`

Індекс, яким необхідно видалити значення.

### Значення, що повертаються

Віддалене значення.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md)якщо індекс некоректний.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::remove()****

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence->remove(1));
var_dump($sequence->remove(0));
var_dump($sequence->remove(0));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "b"
string(1) "a"
string(1) "c"
```
