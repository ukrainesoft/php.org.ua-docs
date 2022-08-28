Метод зберігає набір у пам'яті на диску

-   [« QuickHashIntSet::loadFromString](quickhashintset.loadfromstring.html)
    
-   [QuickHashIntSet::saveToString »](quickhashintset.savetostring.html)
    
-   [PHP Manual](index.html)
    
-   [QuickHashIntSet](class.quickhashintset.html)
    
-   Метод зберігає набір у пам'яті на диску
    

# QuickHashIntSet::saveToFile

(PECL quickhash >= Unknown)

QuickHashIntSet::saveToFile — Метод зберігає набір у пам'яті на диску

### Опис

```methodsynopsis
public QuickHashIntSet::saveToFile(string $filename): void
```

Цей метод зберігає існуючий набір файлу на диску в такому ж форматі, який може бути прочитаний методом [QuickHashIntSet::loadFromFile()](quickhashintset.loadfromfile.html)

### Список параметрів

`filename`

Ім'я файлу, в якому зберігатиметься хеш.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntSet::saveToFile()****

```php
<?php
$set = new QuickHashIntSet( 1024 );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );

$set->saveToFile( '/tmp/test.set' );
?>
```