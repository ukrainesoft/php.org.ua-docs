Метод зберігає хеш у пам'яті на диску

-   [« QuickHashStringIntHash::loadFromString](quickhashstringinthash.loadfromstring.html)
    
-   [QuickHashStringIntHash::saveToString »](quickhashstringinthash.savetostring.html)
    
-   [PHP Manual](index.html)
    
-   [QuickHashStringIntHash](class.quickhashstringinthash.html)
    
-   Метод зберігає хеш у пам'яті на диску
    

# QuickHashStringIntHash::saveToFile

(No version information available, might only be in Git)

QuickHashStringIntHash::saveToFile — Метод зберігає хеш у пам'яті на диску

### Опис

```methodsynopsis
public QuickHashStringIntHash::saveToFile(string $filename): void
```

Метод зберігає існуючий хеш у файл на диску, у тому ж форматі, який може бути прочитаний методом [QuickHashStringIntHash::loadFromFile()](quickhashstringinthash.loadfromfile.html)

### Список параметрів

`filename`

Ім'я файлу, в якому зберігатиметься хеш.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **QuickHashStringIntHash::saveToFile()****

```php
<?php
$hash = new QuickHashStringIntHash( 1024 );
var_dump( $hash->add( "сорок три", 42 ) );
var_dump( $hash->add( "пятьдесят два", 52 ) );

$hash->saveToFile( '/tmp/test.hash.string' );
?>
```