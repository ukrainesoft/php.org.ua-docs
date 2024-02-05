---
navigation:
  - quickhashintset.construct.md: '« QuickHashIntSet::\_\_construct'
  - quickhashintset.exists.md: 'QuickHashIntSet::exists »'
  - index.md: PHP Manual
  - class.quickhashintset.md: QuickHashIntSet
title: 'QuickHashIntSet::delete'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Метод возвращает\*\*`true`\*\*, якщо запис було видалено та **`false`**, якщо запис не видалено.

### Приклади

**Приклад #1 Приклад використання** QuickHashIntSet::delete()\*\*\*\*

```php
<?php
$set = new QuickHashIntSet( 1024 );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );
var_dump( $set->delete( 4 ) );
var_dump( $set->exists( 4 ) );
var_dump( $set->delete( 4 ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
bool(true)
bool(false)
bool(false)
```
