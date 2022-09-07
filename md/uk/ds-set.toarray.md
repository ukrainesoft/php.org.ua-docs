---
navigation:
  - ds-set.sum.md: '« DsSet::sum'
  - ds-set.union.md: 'ДсSet::union »'
  - index.md: PHP Manual
  - class.ds-set.md: Набор
title: 'ДсSet::toArray'
---
# ДсSet::toArray

(PECL ds >= 1.0.0)

ДсSet::toArray — Перетворює колекцію на масив (array)

### Опис

```methodsynopsis
public Ds\Set::toArray(): array
```

Перетворює колекцію на масив (array).

> **Зауваження**
> 
> Приведення до типу array поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array), що містить всі елементи колекції зі збереженням їхнього порядку.

### Приклади

**Приклад #1 Приклад використання **ДсSet::toArray()****

```php
<?php
$set = new \Ds\Set([1, 2, 3]);

var_dump($set->toArray());
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
