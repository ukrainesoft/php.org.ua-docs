---
navigation:
  - quickhashinthash.savetofile.md: '« QuickHashIntHash::saveToFile'
  - quickhashinthash.set.md: 'QuickHashIntHash::set »'
  - index.md: PHP Manual
  - class.quickhashinthash.md: QuickHashIntHash
title: 'QuickHashIntHash::saveToString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntHash::saveToString

(PECL quickhash >= Unknown)

QuickHashIntHash::saveToString — Метод повертає серіалізовану версію хешу

### Опис

```methodsynopsis
public QuickHashIntHash::saveToString(): string
```

Метод повертає серіалізовану версію хешу, у тому форматі, який можна прочитати методом [QuickHashIntHash::loadFromString()](quickhashinthash.loadfromstring.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод повертає рядок, який містить серіалізований формат хешу. Кожен елемент зберігається як 4-байтове значення із порядком байтів, який використовує поточна система.

### Приклади

**Приклад #1 Приклад використання** QuickHashIntHash::saveToString()\*\*\*\*

```php
<?php
$hash = new QuickHashIntHash( 1024 );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, 34 ) );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, 55 ) );

var_dump( $hash->saveToString() );
?>
```
