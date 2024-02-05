---
navigation:
  - ds-sequence.first.md: '« Ds\\Sequence::first'
  - ds-sequence.insert.md: 'Ds\\Sequence::insert »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::get

(PECL ds >= 1.0.0)

Ds\\Sequence::get — Повертає значення за індексом

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

**Приклад #1 Приклад використання** Ds\\Sequence::get()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence->get(0));
var_dump($sequence->get(1));
var_dump($sequence->get(2));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "a"
string(1) "b"
string(1) "c"
```

**Приклад #2 Приклад використання** Ds\\Sequence::get()\*\* із синтаксисом масиву\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence[0]);
var_dump($sequence[1]);
var_dump($sequence[2]);
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "a"
string(1) "b"
string(1) "c"
```
