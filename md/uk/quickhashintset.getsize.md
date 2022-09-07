---
navigation:
  - quickhashintset.exists.md: '« QuickHashIntSet::exists'
  - quickhashintset.loadfromfile.md: 'QuickHashIntSet::loadFromFile »'
  - index.md: PHP Manual
  - class.quickhashintset.md: QuickHashIntSet
title: 'QuickHashIntSet::getSize'
---
# QuickHashIntSet::getSize

(PECL quickhash >= Unknown)

QuickHashIntSet::getSize — Повертає кількість елементів у наборі

### Опис

```methodsynopsis
publicQuickHashIntSet::getSize(): int
```

Повертає кількість елементів у наборі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість елементів у наборі.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntSet::getSize()****

```php
<?php
$set = new QuickHashIntSet( 8 );
var_dump( $set->add( 2 ) );
var_dump( $set->add( 3 ) );
var_dump( $set->getSize() );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(true)
int(2)
```
