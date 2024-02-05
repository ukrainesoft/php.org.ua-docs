---
navigation:
  - ds-vector.rotate.md: '« Ds\\Vector::rotate'
  - ds-vector.shift.md: 'Ds\\Vector::shift »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::set

(PECL ds >= 1.0.0)

Ds\\Vector::set — Замінює значення за вказаним індексом

### Опис

```methodsynopsis
public Ds\Vector::set(int $index, mixed $value): void
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

**Приклад #1 Приклад використання** Ds\\Vector::set()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

$vector->set(1, "_");
print_r($vector);
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

**Приклад #2 Приклад використання** Ds\\Vector::set()\*\* із синтаксисом масиву\*\*

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

$vector[1] = "_";
print_r($vector);
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
