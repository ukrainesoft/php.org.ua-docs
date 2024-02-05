---
navigation:
  - ds-set.sum.md: '« Ds\\Set::sum'
  - ds-set.union.md: 'Ds\\Set::union »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::toArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::toArray

(PECL ds >= 1.0.0)

Ds\\Set::toArray — Перетворює колекцію на масив (array)

### Опис

```methodsynopsis
public Ds\Set::toArray(): array
```

Перетворює колекцію на масив (array).

> **Зауваження** :
> 
> Приведення до типу array поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array), що містить всі елементи колекції, зберігаючи порядок, у якому вони зберігалися.

### Приклади

**Приклад #1 Приклад использования метода**Ds\\Set::toArray()\*\*\*\*

```php
<?php
$set = new \Ds\Set([1, 2, 3]);

var_dump($set->toArray());
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
