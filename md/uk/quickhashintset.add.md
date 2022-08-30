Метод додає новий запис до набору

-   [« QuickHashIntSet](class.quickhashintset.md)
    
-   [QuickHashIntSet::construct »](quickhashintset.construct.md)
    
-   [PHP Manual](index.md)
    
-   [QuickHashIntSet](class.quickhashintset.md)
    
-   Метод додає новий запис до набору
    

# QuickHashIntSet::add

(PECL quickhash >= Unknown)

QuickHashIntSet::add — Метод додає новий запис до набору

### Опис

```methodsynopsis
public QuickHashIntSet::add(int $key): bool
```

Метод додає новий запис у набір і повертає, чи був запис доданий. За умовчанням, додавання відбувається завжди, якщо під час створення хеша не використовувався прапор **`QuickHashIntSet::CHECK_FOR_DUPES`**

### Список параметрів

`key`

Ключ запису, що додається.

### Значення, що повертаються

Метод повертає **`true`**, якщо запис було додано та **`false`**, якщо запис не було додано.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntSet::add()****

```php
<?php
echo "без проверки дубликатов\n";
$set = new QuickHashIntSet( 1024 );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );

echo "\nс проверкой дубликатов\n";
$set = new QuickHashIntSet( 1024, QuickHashIntSet::CHECK_FOR_DUPES );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
без проверки дубликатов
bool(false)
bool(true)
bool(true)
bool(true)

с проверкой дубликатов
bool(false)
bool(true)
bool(true)
bool(false)
```