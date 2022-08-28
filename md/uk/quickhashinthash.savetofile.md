Метод зберігає хеш у пам'яті на диск

-   [« QuickHashIntHash::loadFromString](quickhashinthash.loadfromstring.html)
    
-   [QuickHashIntHash::saveToString »](quickhashinthash.savetostring.html)
    
-   [PHP Manual](index.html)
    
-   [QuickHashIntHash](class.quickhashinthash.html)
    
-   Метод зберігає хеш у пам'яті на диск
    

# QuickHashIntHash::saveToFile

(PECL quickhash >= Unknown)

QuickHashIntHash::saveToFile — Метод зберігає хеш у пам'яті на диск

### Опис

```methodsynopsis
public QuickHashIntHash::saveToFile(string $filename): void
```

Метод зберігає існуючий хеш в пам'яті на диск, у тому форматі, який можна прочитати методом [QuickHashIntHash::loadFromFile()](quickhashinthash.loadfromfile.html)

### Список параметрів

`filename`

Ім'я файлу, в якому зберігатиметься хеш.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntHash::saveToFile()****

```php
<?php
$hash = new QuickHashIntHash( 1024 );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, 43 ) );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, 52 ) );

$hash->saveToFile( '/tmp/test.hash' );
?>
```