---
navigation:
  - ds-set.clear.md: '« Ds\\Set::clear'
  - ds-set.contains.md: 'Ds\\Set::contains »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::\_\_construct

(PECL ds >= 1.0.0)

Ds\\Set::\_\_construct — Створює новий екземпляр класу

### Опис

public**Ds\\Set::\_\_construct** [mixed](language.types.declarations.md#language.types.declarations.mixed) `$values` \[\]) .

Створює новий екземпляр класу, використовуючи або об'єкт, що реалізує [traversable](class.traversable.md), або масив, передані як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Пример #1 Пример использования**Ds\\Set::\_\_construct()\*\*\*\*

```php
<?php
$set = new \Ds\Set();
var_dump($set);

$set = new \Ds\Set([1, 2, 3]);
var_dump($set);
?>
```

Висновок наведеного прикладу буде схожим на:

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
