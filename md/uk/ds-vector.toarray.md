---
navigation:
  - ds-vector.sum.md: '« Ds\\Vector::sum'
  - ds-vector.unshift.md: 'Ds\\Vector::unshift »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::toArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::toArray

(PECL ds >= 1.0.0)

Ds\\Vector::toArray — Перетворює колекцію на масив (array)

### Опис

```methodsynopsis
public Ds\Vector::toArray(): array
```

Перетворює колекцію на масив (array).

> **Зауваження** :
> 
> Приведення до типу array поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array), що містить всі елементи колекції, зберігаючи порядок, у якому вони містилися.

### Приклади

**Приклад #1 Приклад использования метода**Ds\\Vector::toArray()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

var_dump($vector->toArray());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
