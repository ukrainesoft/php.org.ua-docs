---
navigation:
  - ds-collection.copy.md: '« DsCollection::copy'
  - ds-collection.toarray.md: 'ДсCollection::toArray »'
  - index.md: PHP Manual
  - class.ds-collection.md: Коллекция
title: 'ДсCollection::isEmpty'
---
# ДсCollection::isEmpty

(PECL ds >= 1.0.0)

ДсCollection::isEmpty — Перевіряє, чи колекція порожня.

### Опис

```methodsynopsis
abstract public Ds\Collection::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо колекція порожня, та **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад **ДсCollection::isEmpty()****

```php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = new \Ds\Vector();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```
