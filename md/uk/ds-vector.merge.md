---
navigation:
  - ds-vector.map.md: '« Ds\\Vector::map'
  - ds-vector.pop.md: 'Ds\\Vector::pop »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::merge'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::merge

(PECL ds >= 1.0.0)

Ds\\Vector::merge — Повертає результат додавання всіх заданих значень у вектор.

### Опис

```methodsynopsis
public Ds\Vector::merge(mixed $values): Ds\Vector
```

Повертає результат додавання всіх заданих значень вектор.

### Список параметрів

`values`

Об'єкт класу [traversable](class.traversable.md)или массив (array).

### Значення, що повертаються

Результат додавання всіх переданих значень вектор. Фактично робиться копія вектора, який додаються значення.

> **Зауваження** :
> 
> Поточний екземпляр вектора залишиться недоторканим.

### Приклади

**Пример #1 Пример использования**Ds\\Vector::merge()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

var_dump($vector->merge([4, 5, 6]));
var_dump($vector);
?>
```

Висновок наведеного прикладу буде схожим на:

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
