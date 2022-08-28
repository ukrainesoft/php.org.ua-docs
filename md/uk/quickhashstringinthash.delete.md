Метод видаляє запис із хешу

-   [« QuickHashStringIntHash::\_\_construct](quickhashstringinthash.construct.html)
    
-   [QuickHashStringIntHash::exists »](quickhashstringinthash.exists.html)
    
-   [PHP Manual](index.html)
    
-   [QuickHashStringIntHash](class.quickhashstringinthash.html)
    
-   Метод видаляє запис із хешу
    

# QuickHashStringIntHash::delete

(No version information available, might only be in Git)

QuickHashStringIntHash::delete — Метод видаляє запис із хешу

### Опис

```methodsynopsis
public QuickHashStringIntHash::delete(string $key): bool
```

Метод видаляє запис з хеша і повертає, чи цей запис видалено чи ні. Відповідні структури пам'яті буде звільнено не відразу, а при звільненні самого хеша.

Елементи не можна видалити, якщо хеш використовується в ітераторі. Метод не викине виняток, а просто поверне **`false`** як це сталося б за будь-якої іншої помилки видалення.

### Список параметрів

`key`

Ключ запису, який потрібно видалити.

### Значення, що повертаються

Метод повертає **`true`**, якщо запис було видалено та **`false`**, якщо запис не видалено.

### Приклади

**Приклад #1 Приклад використання **QuickHashStringIntHash::delete()****

```php
<?php
$hash = new QuickHashStringIntHash( 1024 );
var_dump( $hash->exists( 'four' ) );
var_dump( $hash->add( 'four', 5 ) );
var_dump( $hash->get( 'four' ) );
var_dump( $hash->delete( 'four' ) );
var_dump( $hash->exists( 'four' ) );
var_dump( $hash->get( 'four' ) );
var_dump( $hash->delete( 'four' ) );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
int(5)
bool(true)
bool(false)
bool(false)
bool(false)
```