---
navigation:
  - ds-vector.map.md: '« DsVector::map'
  - ds-vector.pop.md: 'ДсVector::pop »'
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::merge'
---
# ДсVector::merge

(PECL ds >= 1.0.0)

ДсVector::merge — Повертає результат додавання всіх заданих значень у вектор.

### Опис

```methodsynopsis
public Ds\Vector::merge(mixed $values): Ds\Vector
```

Повертає результат додавання всіх заданих значень вектор.

### Список параметрів

`values`

Об'єкт класу [traversable](class.traversable.md) чи масив (array).

### Значення, що повертаються

Результат додавання всіх переданих значень вектор. Фактично робиться копія вектора, який додаються значення.

> **Зауваження**
> 
> Поточний екземпляр вектора залишиться недоторканим.

### Приклади

**Приклад #1 Приклад використання **ДсVector::merge()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

var_dump($vector->merge([4, 5, 6]));
var_dump($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Vector)#2 (6) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
  [3]=>
  int(4)
  [4]=>
  int(5)
  [5]=>
  int(6)
}
object(Ds\Vector)#1 (3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
