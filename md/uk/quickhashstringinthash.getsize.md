---
navigation:
  - quickhashstringinthash.get.md: '« QuickHashStringIntHash::get'
  - quickhashstringinthash.loadfromfile.md: 'QuickHashStringIntHash::loadFromFile »'
  - index.md: PHP Manual
  - class.quickhashstringinthash.md: QuickHashStringIntHash
title: 'QuickHashStringIntHash::getSize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashStringIntHash::getSize

(No version information available, might only be in Git)

QuickHashStringIntHash::getSize — Повертає кількість елементів у хеші

### Опис

```methodsynopsis
public QuickHashStringIntHash::getSize(): int
```

Повертає кількість елементів у хеші.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод повертає кількість елементів у хеші.

### Приклади

**Приклад #1 Приклад використання** QuickHashStringIntHash::getSize()\*\*\*\*

```php
<?php
$hash = new QuickHashStringIntHash( 8 );
var_dump( $hash->add( "two", 2 ) );
var_dump( $hash->add( "three", 5 ) );
var_dump( $hash->getSize() );
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
int(2)
```
