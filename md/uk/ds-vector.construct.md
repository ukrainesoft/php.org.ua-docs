---
navigation:
  - ds-vector.clear.md: '« Ds\\Vector::clear'
  - ds-vector.contains.md: 'Ds\\Vector::contains »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::\_\_construct

(PECL ds >= 1.0.0)

Ds\\Vector::\_\_construct — Створює новий екземпляр

### Опис

public **Ds\\Vector::\_\_construct** [mixed](language.types.declarations.md#language.types.declarations.mixed) `$values`

Створює новий екземпляр, використовуючи або об'єкт реалізує [traversable](class.traversable.md), або масив, передані як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання** Ds\\Vector::\_\_construct()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector();
var_dump($vector);


$vector = new \Ds\Vector([1, 2, 3]);
var_dump($vector);
?>
```

Висновок наведеного прикладу буде схожим на:

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
