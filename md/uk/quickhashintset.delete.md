---
navigation:
  - quickhashintset.construct.html: '« QuickHashIntSet::construct'
  - quickhashintset.exists.html: 'QuickHashIntSet::exists »'
  - index.html: PHP Manual
  - class.quickhashintset.html: QuickHashIntSet
title: 'QuickHashIntSet::delete'
---
# QuickHashIntSet::delete

(PECL quickhash >= Unknown)

QuickHashIntSet::delete — Метод видаляє запис із набору

### Опис

```methodsynopsis
public QuickHashIntSet::delete(int $key): bool
```

Метод видаляє запис з множини і повертає, був видалений чи ні. Відповідні структури пам'яті буде звільнено не відразу, а при звільненні самого набору.

### Список параметрів

`key`

Ключ запису, який потрібно видалити.

### Значення, що повертаються

Метод повертає **`true`**, якщо запис було видалено та **`false`**, якщо запис не видалено.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntSet::delete()****

```php
<?php
$set = new QuickHashIntSet( 1024 );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );
var_dump( $set->delete( 4 ) );
var_dump( $set->exists( 4 ) );
var_dump( $set->delete( 4 ) );
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
