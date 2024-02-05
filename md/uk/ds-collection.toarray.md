---
navigation:
  - ds-collection.isempty.md: '« Ds\\Collection::isEmpty'
  - class.ds-hashable.md: Ds\\Hashable »
  - index.md: PHP Manual
  - class.ds-collection.md: Ds\\Collection
title: 'Ds\\Collection::toArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Collection::toArray

(PECL ds >= 1.0.0)

Ds\\Collection::toArray — Перетворює колекцію на масив (array)

### Опис

```methodsynopsis
public Ds\Collection::toArray(): array
```

Перетворює колекцію на array.

> **Зауваження** :
> 
> Приведення до масиву (array) не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array), що містить усі елементи колекції у тому порядку.

### Приклади

**Приклад #1 Приклад использования метода**Ds\\Collection::toArray()\*\*\*\*

```php
<?php
$collection = new \Ds\Vector([1, 2, 3]);

var_dump($collection->toArray());
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
