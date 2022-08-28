Повертає кількість елементів у хеші

-   [« QuickHashIntHash::get](quickhashinthash.get.html)
    
-   [QuickHashIntHash::loadFromFile »](quickhashinthash.loadfromfile.html)
    
-   [PHP Manual](index.html)
    
-   [QuickHashIntHash](class.quickhashinthash.html)
    
-   Повертає кількість елементів у хеші
    

# QuickHashIntHash::getSize

(PECL quickhash >= Unknown)

QuickHashIntHash::getSize — Повертає кількість елементів у хеші

### Опис

```methodsynopsis
public QuickHashIntHash::getSize(): int
```

Повертає кількість елементів у хеші.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод повертає кількість елементів у хеші.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntHash::getSize()****

```php
<?php
$hash = new QuickHashIntHash( 8 );
var_dump( $hash->add( 2 ) );
var_dump( $hash->add( 3, 5 ) );
var_dump( $hash->getSize() );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(true)
int(2)
```