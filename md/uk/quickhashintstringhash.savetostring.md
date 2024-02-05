---
navigation:
  - quickhashintstringhash.savetofile.md: '« QuickHashIntStringHash::saveToFile'
  - quickhashintstringhash.set.md: 'QuickHashIntStringHash::set »'
  - index.md: PHP Manual
  - class.quickhashintstringhash.md: QuickHashIntStringHash
title: 'QuickHashIntStringHash::saveToString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntStringHash::saveToString

(PECL quickhash >= Unknown)

QuickHashIntStringHash::saveToString — Метод повертає серіалізовану версію хешу

### Опис

```methodsynopsis
public QuickHashIntStringHash::saveToString(): string
```

Метод повертає серіалізовану версію хешу у тому ж форматі, який може бути прочитаний методом [QuickHashIntStringHash::loadFromString()](quickhashintstringhash.loadfromstring.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод повертає рядок, який містить серіалізовану версію хеша. Кожен елемент зберігається як чотири байтове значення в системному порядку байтів.

### Приклади

**Пример #1 Пример использования**QuickHashIntStringHash::saveToString()\*\*\*\*

```php
<?php
$hash = new QuickHashIntStringHash( 1024 );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, "тридцать четыре" ) );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 5, "пятьдесят пять" ) );

var_dump( $hash->saveToString() );
?>
```
