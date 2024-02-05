---
navigation:
  - ds-set.last.md: '« Ds\\Set::last'
  - ds-set.reduce.md: 'Ds\\Set::reduce »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::merge'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::merge

(PECL ds >= 1.0.3)

Ds\\Set::merge — Повертає результат додавання всіх заданих значень до набору

### Опис

```methodsynopsis
public Ds\Set::merge(mixed $values): Ds\Set
```

Повертає результат додавання всіх заданих значень до набору.

### Список параметрів

`values`

Об'єкт класу [traversable](class.traversable.md)или массив (array).

### Значення, що повертаються

Результат додавання всіх переданих значень до набору. Фактично робиться копія набору, до якої додаються значення.

> **Зауваження** :
> 
> Поточний екземпляр набору залишиться недоторканим.

### Приклади

**Пример #1 Пример использования**Ds\\Set::merge()\*\*\*\*

```php
<?php
$set = new \Ds\Set([1, 2, 3]);

var_dump($set->merge([3, 4, 5]));
var_dump($set);
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Set)#2 (6) {
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
}
object(Ds\Set)#1 (3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
