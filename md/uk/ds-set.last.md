---
navigation:
  - ds-set.jsonserialize.md: '« DsSet::jsonSerialize'
  - ds-set.merge.md: 'ДсSet::merge »'
  - index.md: PHP Manual
  - class.ds-set.md: Набор
title: 'ДсSet::last'
---
# ДсSet::last

(PECL ds >= 1.0.0)

ДсSet::last — Повертає останнє значення колекції

### Опис

```methodsynopsis
public Ds\Set::last(): mixed
```

Повертає останнє значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент колекції.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання **ДсSet::last()****

```php
<?php
$set = new \Ds\Set([1, 2, 3]);
var_dump($set->last());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(3)
```
