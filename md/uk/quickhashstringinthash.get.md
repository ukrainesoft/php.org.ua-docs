Метод отримує значення з хеша за його ключем

-   [« QuickHashStringIntHash::exists](quickhashstringinthash.exists.html)
    
-   [QuickHashStringIntHash::getSize »](quickhashstringinthash.getsize.html)
    
-   [PHP Manual](index.html)
    
-   [QuickHashStringIntHash](class.quickhashstringinthash.html)
    
-   Метод отримує значення з хеша за його ключем
    

# QuickHashStringIntHash::get

(No version information available, might only be in Git)

QuickHashStringIntHash::get — Метод витягує значення з хеша за його ключем

### Опис

```methodsynopsis
public QuickHashStringIntHash::get(string $key): mixed
```

Метод отримує значення з хеша за його ключем.

### Список параметрів

`key`

Ключ одержуваного запису.

### Значення, що повертаються

Метод повертає значення, якщо ключ існує або **`null`**якщо ключ не є частиною хеша.

### Приклади

**Приклад #1 Приклад використання **QuickHashStringIntHash::get()****

```php
<?php
$hash = new QuickHashStringIntHash( 8 );
var_dump( $hash->get( "one" ) );

var_dump( $hash->add( "two", 2 ) );
var_dump( $hash->get( "two" ) );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
int(2)
```