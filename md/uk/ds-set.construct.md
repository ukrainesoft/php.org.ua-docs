---
navigation:
  - ds-set.clear.md: '« DsSet::clear'
  - ds-set.contains.md: 'ДсSet::contains »'
  - index.md: PHP Manual
  - class.ds-set.md: Набор
title: 'ДсSet::construct'
---
# ДсSet::construct

(PECL ds >= 1.0.0)

ДсSet::construct — Створює новий екземпляр класу

### Опис

public **ДсSet::construct**[mixed](language.types.declarations.md#language.types.declarations.mixed) `$values`

Створює новий екземпляр класу, використовуючи або об'єкт, що реалізує [traversable](class.traversable.md), або масив, передані як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання **ДсSet::construct()****

```php
<?php
$set = new \Ds\Set();
var_dump($set);

$set = new \Ds\Set([1, 2, 3]);
var_dump($set);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Set)#1 (0) {
}
object(Ds\Set)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
