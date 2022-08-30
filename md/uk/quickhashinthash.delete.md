Метод видаляє запис із хешу

-   [« QuickHashIntHash::construct](quickhashinthash.construct.md)
    
-   [QuickHashIntHash::exists »](quickhashinthash.exists.md)
    
-   [PHP Manual](index.md)
    
-   [QuickHashIntHash](class.quickhashinthash.md)
    
-   Метод видаляє запис із хешу
    

# QuickHashIntHash::delete

(PECL quickhash >= Unknown)

QuickHashIntHash::delete — Метод видаляє запис із хешу

### Опис

```methodsynopsis
public QuickHashIntHash::delete(int $key): bool
```

Метод видаляє запис з хеша і повертає, чи цей запис видалено чи ні. Відповідні структури пам'яті буде звільнено не відразу, а при звільненні самого хеша.

Елементи не можна видалити, якщо хеш використовується в ітераторі. Метод не викине виняток, а просто поверне **`false`** як це сталося б за будь-якої іншої помилки видалення.

### Список параметрів

`key`

Ключ запису, який потрібно видалити.

### Значення, що повертаються

Метод повертає **`true`**, якщо запис було видалено та **`false`**, якщо запис не видалено.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntHash::delete()****

```php
<?php

$hash = new QuickHashIntHash( 1024 );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, 5 ) );
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