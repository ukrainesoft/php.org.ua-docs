---
navigation:
  - ds-collection.clear.html: '« DsCollection::clear'
  - ds-collection.isempty.html: 'ДсCollection::isEmpty »'
  - index.html: PHP Manual
  - class.ds-collection.html: Коллекция
title: 'ДсCollection::copy'
---
# ДсCollection::copy

(PECL ds >= 1.0.0)

ДсCollection::copy — Повертає копію колекції

### Опис

```methodsynopsis
abstract public Ds\Collection::copy(): Ds\Collection
```

Повертає копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає копію колекції.

### Приклади

**Приклад #1 Приклад **ДсCollection::copy()****

```php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = $a->copy();

$b->push(4);

print_r($a);
print_r($b);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
)
```
