---
navigation:
  - ds-sequence.map.md: '« Ds\\Sequence::map'
  - ds-sequence.pop.md: 'Ds\\Sequence::pop »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::merge'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::merge

(PECL ds >= 1.0.0)

Ds\\Sequence::merge — Повертає результат додавання всіх заданих значень до колекції

### Опис

```methodsynopsis
abstract public Ds\Sequence::merge(mixed $values): Ds\Sequence
```

Повертає результат додавання всіх заданих значень до колекції.

### Список параметрів

`values`

Об'єкт класу [traversable](class.traversable.md)или array.

### Значення, що повертаються

Результат додавання всіх переданих значень до колекції. Фактично робиться копія колекції, до якої додаються значення.

> **Зауваження** :
> 
> Поточний екземпляр колекції залишиться недоторканим.

### Приклади

**Приклад #1 Приклад використання** Ds\\Sequence::merge()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

var_dump($sequence->merge([4, 5, 6]));
var_dump($sequence);
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
