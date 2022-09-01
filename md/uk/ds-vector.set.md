---
navigation:
  - ds-vector.rotate.html: '« DsVector::rotate'
  - ds-vector.shift.html: 'ДсVector::shift »'
  - index.md: PHP Manual
  - class.ds-vector.html: Вектор
title: 'ДсVector::set'
---
# ДсVector::set

(PECL ds >= 1.0.0)

ДсVector::set — Замінює значення за вказаним індексом

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

**Приклад #1 Приклад використання **ДсVector::set()****

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

$vector->set(1, "_");
print_r($vector);
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

**Приклад #2 Приклад використання **ДсVector::set()** із синтаксисом масиву**

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

$vector[1] = "_";
print_r($vector);
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
