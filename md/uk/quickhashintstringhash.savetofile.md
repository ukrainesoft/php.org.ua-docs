---
navigation:
  - quickhashintstringhash.loadfromstring.md: '« QuickHashIntStringHash::loadFromString'
  - quickhashintstringhash.savetostring.md: 'QuickHashIntStringHash::saveToString »'
  - index.md: PHP Manual
  - class.quickhashintstringhash.md: QuickHashIntStringHash
title: 'QuickHashIntStringHash::saveToFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntStringHash::saveToFile

(PECL quickhash >= Unknown)

QuickHashIntStringHash::saveToFile — Метод зберігає хеш у пам'яті на диску

### Опис

```methodsynopsis
public QuickHashIntStringHash::saveToFile(string $filename): void
```

Метод зберігає існуючий хеш у файл на диску, у тому форматі, який може бути прочитаний методом [QuickHashIntStringHash::loadFromFile()](quickhashintstringhash.loadfromfile.md)

### Список параметрів

`filename`

Ім'я файлу, в якому зберігатиметься хеш.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**QuickHashIntStringHash::saveToFile()\*\*\*\*

```php
<?php
$hash = new QuickHashIntStringHash( 1024 );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, "сорок три" ) );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, "пятьдесят два" ) );

$hash->saveToFile( '/tmp/test.string.hash' );
?>
```
