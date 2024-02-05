---
navigation:
  - quickhashintset.savetofile.md: '« QuickHashIntSet::saveToFile'
  - class.quickhashinthash.md: QuickHashIntHash »
  - index.md: PHP Manual
  - class.quickhashintset.md: QuickHashIntSet
title: 'QuickHashIntSet::saveToString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntSet::saveToString

(PECL quickhash >= Unknown)

QuickHashIntSet::saveToString — Метод повертає серіалізовану версію набору

### Опис

```methodsynopsis
public QuickHashIntSet::saveToString(): string
```

Метод повертає серіалізовану версію набору в тому ж форматі, що може бути прочитаний методом [QuickHashIntSet::loadFromString()](quickhashintset.loadfromstring.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод повертає рядок, який містить серіалізовану версію набору. Кожен елемент зберігається як чотири байтове значення в системному порядку байтів.

### Приклади

**Приклад #1 Приклад використання** QuickHashIntSet::saveToString()\*\*\*\*

```php
<?php
$set = new QuickHashIntSet( 1024 );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );

var_dump( $set->saveToString() );
?>
```
