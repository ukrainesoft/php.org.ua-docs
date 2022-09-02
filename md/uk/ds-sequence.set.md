---
navigation:
  - ds-sequence.rotate.md: '« DsSequence::rotate'
  - ds-sequence.shift.md: 'ДсSequence::shift »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Послідовність
title: 'ДсSequence::set'
---
# ДсSequence::set

(PECL ds >= 1.0.0)

ДсSequence::set — Замінює значення за вказаним індексом

### Опис

```methodsynopsis
abstract public Ds\Sequence::set(int $index, mixed $value): void
```

Замінює значення за вказаним індексом.

### Список параметрів

`index`

Індекс, яким треба замінити значення.

`value`

Нове значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md)якщо індекс некоректний.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::set()****

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

$sequence->set(1, "_");
print_r($sequence);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => a
    [1] => _
    [2] => c
)
```

**Приклад #2 Приклад використання **ДсSequence::set()** із синтаксисом масиву**

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

$sequence[1] = "_";
print_r($sequence);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => a
    [1] => _
    [2] => c
)
```
