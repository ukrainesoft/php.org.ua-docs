---
navigation:
  - ds-collection.isempty.md: '« DsCollection::isEmpty'
  - class.ds-hashable.md: Хешируемое »
  - index.md: PHP Manual
  - class.ds-collection.md: Коллекция
title: 'ДсCollection::toArray'
---
# ДсCollection::toArray

(PECL ds >= 1.0.0)

ДсCollection::toArray — Перетворює колекцію на масив (array)

### Опис

```methodsynopsis
abstract public Ds\Collection::toArray(): array
```

Перетворює колекцію на array.

> **Зауваження**
> 
> Приведення до масиву (array) на даний момент не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array), що містить усі елементи колекції у тому порядку.

### Приклади

**Приклад #1 Приклад **ДсCollection::toArray()****

```php
<?php
$collection = new \Ds\Vector([1, 2, 3]);

var_dump($collection->toArray());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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
