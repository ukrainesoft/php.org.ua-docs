---
navigation:
  - quickhashinthash.get.md: '« QuickHashIntHash::get'
  - quickhashinthash.loadfromfile.md: 'QuickHashIntHash::loadFromFile »'
  - index.md: PHP Manual
  - class.quickhashinthash.md: QuickHashIntHash
title: 'QuickHashIntHash::getSize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntHash::getSize

(PECL quickhash >= Unknown)

QuickHashIntHash::getSize — Повертає кількість елементів у хеші

### Опис

```methodsynopsis
public QuickHashIntHash::getSize(): int
```

Повертає кількість елементів у хеші.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод повертає кількість елементів у хеші.

### Приклади

**Приклад #1 Приклад використання** QuickHashIntHash::getSize()\*\*\*\*

```php
<?php
$hash = new QuickHashIntHash( 8 );
var_dump( $hash->add( 2 ) );
var_dump( $hash->add( 3, 5 ) );
var_dump( $hash->getSize() );
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
int(2)
```
