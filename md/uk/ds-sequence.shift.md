---
navigation:
  - ds-sequence.set.html: '« DsSequence::set'
  - ds-sequence.slice.html: 'ДсSequence::slice »'
  - index.md: PHP Manual
  - class.ds-sequence.html: Послідовність
title: 'ДсSequence::shift'
---
# ДсSequence::shift

(PECL ds >= 1.0.0)

ДсSequence::shift — Видаляє та повертає перше значення

### Опис

```methodsynopsis
abstract public Ds\Sequence::shift(): mixed
```

Видаляє та повертає перше значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перше віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::shift()****

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence->shift());
var_dump($sequence->shift());
var_dump($sequence->shift());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```
