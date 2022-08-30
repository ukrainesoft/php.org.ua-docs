Метод видаляє запис із хешу

-   [« QuickHashIntStringHash::construct](quickhashintstringhash.construct.md)
    
-   [QuickHashIntStringHash::exists »](quickhashintstringhash.exists.md)
    
-   [PHP Manual](index.md)
    
-   [QuickHashIntStringHash](class.quickhashintstringhash.md)
    
-   Метод видаляє запис із хешу
    

# QuickHashIntStringHash::delete

(PECL quickhash >= Unknown)

QuickHashIntStringHash::delete — Метод видаляє запис із хешу

### Опис

```methodsynopsis
public QuickHashIntStringHash::delete(int $key): bool
```

Метод видаляє запис з хеша і повертає, чи цей запис видалено чи ні. Відповідні структури пам'яті буде звільнено не відразу, а при звільненні самого хеша.

Елементи не можна видалити, якщо хеш використовується в ітераторі. Метод не викине виняток, а просто поверне **`false`**, як це сталося б за будь-якої іншої помилки видалення.

### Список параметрів

`key`

Ключ запису, що видаляється.

### Значення, що повертаються

Метод повертає **`true`**, якщо запис було видалено та **`false`**, якщо запис не видалено.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntStringHash::delete()****

```php
<?php
$hash = new QuickHashIntStringHash( 1024 );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, "five" ) );
var_dump( $hash->delete( 4 ) );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->delete( 4 ) );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
bool(true)
bool(false)
bool(false)
```