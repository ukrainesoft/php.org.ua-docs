---
navigation:
  - quickhashstringinthash.savetofile.html: '« QuickHashStringIntHash::saveToFile'
  - quickhashstringinthash.set.html: 'QuickHashStringIntHash::set »'
  - index.html: PHP Manual
  - class.quickhashstringinthash.html: QuickHashStringIntHash
title: 'QuickHashStringIntHash::saveToString'
---
# QuickHashStringIntHash::saveToString

(No version information available, might only be in Git)

QuickHashStringIntHash::saveToString — Метод повертає серіалізовану версію хешу

### Опис

```methodsynopsis
public QuickHashStringIntHash::saveToString(): string
```

Метод повертає серіалізовану версію хешу у тому ж форматі, який може бути прочитаний методом [QuickHashStringIntHash::loadFromString()](quickhashstringinthash.loadfromstring.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод повертає серіалізовану версію хешу у тому ж форматі, який може бути прочитаний методом [QuickHashStringIntHash::loadFromString()](quickhashstringinthash.loadfromstring.html)

### Приклади

**Приклад #1 Приклад використання **QuickHashStringIntHash::saveToString()****

```php
<?php
$hash = new QuickHashStringIntHash( 1024 );
var_dump( $hash->add( "сорок три", 42 ) );
var_dump( $hash->add( "пятьдесят два", 52 ) );

var_dump( $hash->saveToString() );
?>
```
