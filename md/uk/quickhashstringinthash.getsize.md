Повертає кількість елементів у хеші

-   [« QuickHashStringIntHash::get](quickhashstringinthash.get.md)
    
-   [QuickHashStringIntHash::loadFromFile »](quickhashstringinthash.loadfromfile.md)
    
-   [PHP Manual](index.md)
    
-   [QuickHashStringIntHash](class.quickhashstringinthash.md)
    
-   Повертає кількість елементів у хеші
    

# QuickHashStringIntHash::getSize

(No version information available, might only be in Git)

QuickHashStringIntHash::getSize — Повертає кількість елементів у хеші

### Опис

```methodsynopsis
public QuickHashStringIntHash::getSize(): int
```

Повертає кількість елементів у хеші.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод повертає кількість елементів у хеші.

### Приклади

**Приклад #1 Приклад використання **QuickHashStringIntHash::getSize()****

```php
<?php
$hash = new QuickHashStringIntHash( 8 );
var_dump( $hash->add( "two", 2 ) );
var_dump( $hash->add( "three", 5 ) );
var_dump( $hash->getSize() );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(true)
int(2)
```