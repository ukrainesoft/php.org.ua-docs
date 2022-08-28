Метод зберігає хеш у пам'яті на диску

-   [« QuickHashIntStringHash::loadFromString](quickhashintstringhash.loadfromstring.html)
    
-   [QuickHashIntStringHash::saveToString »](quickhashintstringhash.savetostring.html)
    
-   [PHP Manual](index.html)
    
-   [QuickHashIntStringHash](class.quickhashintstringhash.html)
    
-   Метод зберігає хеш у пам'яті на диску
    

# QuickHashIntStringHash::saveToFile

(PECL quickhash >= Unknown)

QuickHashIntStringHash::saveToFile — Метод зберігає хеш у пам'яті на диску

### Опис

```methodsynopsis
public QuickHashIntStringHash::saveToFile(string $filename): void
```

Метод зберігає існуючий хеш у файл на диску, у тому ж форматі, який може бути прочитаний методом [QuickHashIntStringHash::loadFromFile()](quickhashintstringhash.loadfromfile.html)

### Список параметрів

`filename`

Ім'я файлу, в якому зберігатиметься хеш.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntStringHash::saveToFile()****

```php
<?php
$hash = new QuickHashIntStringHash( 1024 );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, "сорок три" ) );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, "пятьдесят два" ) );

$hash->saveToFile( '/tmp/test.string.hash' );
?>
```