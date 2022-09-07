---
navigation:
  - ds-set.allocate.md: '« DsSet::allocate'
  - ds-set.clear.md: 'ДсSet::clear »'
  - index.md: PHP Manual
  - class.ds-set.md: Набор
title: 'ДсSet::capacity'
---
# ДсSet::capacity

(PECL ds >= 1.0.0)

ДсSet::capacity — Повертає поточну місткість

### Опис

```methodsynopsis
public Ds\Set::capacity(): int
```

Повертає поточну місткість.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна місткість.

### Приклади

**Приклад #1 Приклад використання **ДсSet::capacity()****

```php
<?php
$set = new \Ds\Set();
var_dump($set->capacity());

$set->push(...range(1, 50));
var_dump($set->capacity());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(16)
int(64)
```
