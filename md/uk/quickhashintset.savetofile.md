---
navigation:
  - quickhashintset.loadfromstring.md: '« QuickHashIntSet::loadFromString'
  - quickhashintset.savetostring.md: 'QuickHashIntSet::saveToString »'
  - index.md: PHP Manual
  - class.quickhashintset.md: QuickHashIntSet
title: 'QuickHashIntSet::saveToFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntSet::saveToFile

(PECL quickhash >= Unknown)

QuickHashIntSet::saveToFile — Метод зберігає набір у пам'яті на диску

### Опис

```methodsynopsis
public QuickHashIntSet::saveToFile(string $filename): void
```

Цей метод зберігає існуючий набір файлу на диску в такому ж форматі, який може бути прочитаний методом [QuickHashIntSet::loadFromFile()](quickhashintset.loadfromfile.md)

### Список параметрів

`filename`

Ім'я файлу, в якому зберігатиметься хеш.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**QuickHashIntSet::saveToFile()\*\*\*\*

```php
<?php
$set = new QuickHashIntSet( 1024 );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );

$set->saveToFile( '/tmp/test.set' );
?>
```
