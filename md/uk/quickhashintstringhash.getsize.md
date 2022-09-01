---
navigation:
  - quickhashintstringhash.get.html: '« QuickHashIntStringHash::get'
  - quickhashintstringhash.loadfromfile.html: 'QuickHashIntStringHash::loadFromFile »'
  - index.html: PHP Manual
  - class.quickhashintstringhash.html: QuickHashIntStringHash
title: 'QuickHashIntStringHash::getSize'
---
# QuickHashIntStringHash::getSize

(PECL quickhash >= Unknown)

QuickHashIntStringHash::getSize — Повертає кількість елементів у хеші

### Опис

```methodsynopsis
public QuickHashIntStringHash::getSize(): int
```

Повертає кількість елементів у хеші.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість елементів у хеш.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntStringHash::getSize()****

```php
<?php
$hash = new QuickHashIntStringHash( 8 );
var_dump( $hash->add( 2, "two" ) );
var_dump( $hash->add( 3, 5 ) );
var_dump( $hash->getSize() );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(true)
int(2)
```
