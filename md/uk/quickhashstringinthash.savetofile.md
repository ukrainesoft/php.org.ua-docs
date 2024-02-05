---
navigation:
  - quickhashstringinthash.loadfromstring.md: '« QuickHashStringIntHash::loadFromString'
  - quickhashstringinthash.savetostring.md: 'QuickHashStringIntHash::saveToString »'
  - index.md: PHP Manual
  - class.quickhashstringinthash.md: QuickHashStringIntHash
title: 'QuickHashStringIntHash::saveToFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashStringIntHash::saveToFile

(No version information available, might only be in Git)

QuickHashStringIntHash::saveToFile — Метод зберігає хеш у пам'яті на диску

### Опис

```methodsynopsis
public QuickHashStringIntHash::saveToFile(string $filename): void
```

Метод зберігає існуючий хеш у файл на диску, у тому форматі, який може бути прочитаний методом [QuickHashStringIntHash::loadFromFile()](quickhashstringinthash.loadfromfile.md)

### Список параметрів

`filename`

Ім'я файлу, в якому зберігатиметься хеш.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**QuickHashStringIntHash::saveToFile()\*\*\*\*

```php
<?php
$hash = new QuickHashStringIntHash( 1024 );
var_dump( $hash->add( "сорок три", 42 ) );
var_dump( $hash->add( "пятьдесят два", 52 ) );

$hash->saveToFile( '/tmp/test.hash.string' );
?>
```
