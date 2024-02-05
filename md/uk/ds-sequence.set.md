---
navigation:
  - ds-sequence.rotate.md: '« Ds\\Sequence::rotate'
  - ds-sequence.shift.md: 'Ds\\Sequence::shift »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::set

(PECL ds >= 1.0.0)

Ds\\Sequence::set — Замінює значення за вказаним індексом

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

**Приклад #1 Приклад використання** Ds\\Sequence::set()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

$sequence->set(1, "_");
print_r($sequence);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Vector Object
(
    [0] => a
    [1] => _
    [2] => c
)
```

**Приклад #2 Приклад використання** Ds\\Sequence::set()\*\* із синтаксисом масиву\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

$sequence[1] = "_";
print_r($sequence);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Vector Object
(
    [0] => a
    [1] => _
    [2] => c
)
```
