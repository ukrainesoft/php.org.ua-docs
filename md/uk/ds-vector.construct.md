---
navigation:
  - ds-vector.clear.md: '« DsVector::clear'
  - ds-vector.contains.md: 'ДсVector::contains »'
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::construct'
---
# ДсVector::construct

(PECL ds >= 1.0.0)

ДсVector::construct — Створює новий екземпляр

### Опис

public **ДсVector::construct**[mixed](language.types.declarations.md#language.types.declarations.mixed) `$values`

Створює новий екземпляр, використовуючи або об'єкт реалізує [traversable](class.traversable.md), або масив, передані як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання **ДсVector::construct()****

```php
<?php
$vector = new \Ds\Vector();
var_dump($vector);


$vector = new \Ds\Vector([1, 2, 3]);
var_dump($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Vector)#2 (0) {
}
object(Ds\Vector)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
