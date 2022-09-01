---
navigation:
  - ds-sequence.first.html: '« DsSequence::first'
  - ds-sequence.insert.html: 'ДсSequence::insert »'
  - index.md: PHP Manual
  - class.ds-sequence.html: Послідовність
title: 'ДсSequence::get'
---
# ДсSequence::get

(PECL ds >= 1.0.0)

ДсSequence::get — Повертає значення за індексом

### Опис

```methodsynopsis
abstract public Ds\Sequence::get(int $index): mixed
```

Повертає значення за заданим індексом.

### Список параметрів

`index`

Індекс. Перший елемент має індекс 0.

### Значення, що повертаються

Значення за заданим індексом.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md)якщо індекс некоректний.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::get()****

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence->get(0));
var_dump($sequence->get(1));
var_dump($sequence->get(2));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```

**Приклад #2 Приклад використання **ДсSequence::get()** із синтаксисом масиву**

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence[0]);
var_dump($sequence[1]);
var_dump($sequence[2]);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```
