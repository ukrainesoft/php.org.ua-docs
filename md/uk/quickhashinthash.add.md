---
navigation:
  - class.quickhashinthash.md: « QuickHashIntHash
  - quickhashinthash.construct.md: 'QuickHashIntHash::\_\_construct »'
  - index.md: PHP Manual
  - class.quickhashinthash.md: QuickHashIntHash
title: 'QuickHashIntHash::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntHash::add

(PECL quickhash >= Unknown)

QuickHashIntHash::add — Додати елемент у хеш

### Опис

```methodsynopsis
public QuickHashIntHash::add(int $key, int $value = ?): bool
```

Додає елемент у хеш та повертає **`true`** або **`false`**в зависимости от успешности операции. По умолчанию, добавление происходит всегда, если при создании хеша не использовался флаг**`QuickHashIntHash::CHECK_FOR_DUPES`**

### Список параметрів

`key`

Ключ запису, що додається.

`value`

Опціональне значення. Якщо не задано, то використовуватиметься

### Значення, що повертаються

У разі вдалого додавання повертає **`true`**. У разі невдалого - **`false`**

### Приклади

**Приклад #1 Приклад використання** QuickHashIntHash::add()\*\*\*\*

```php
<?php
echo "without dupe checking\n";
$hash = new QuickHashIntHash( 1024 );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->get( 4 ) );
var_dump( $hash->add( 4, 22 ) );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->get( 4 ) );
var_dump( $hash->add( 4, 12 ) );

echo "\nwith dupe checking\n";
$hash = new QuickHashIntHash( 1024, QuickHashIntHash::CHECK_FOR_DUPES );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->get( 4 ) );
var_dump( $hash->add( 4, 78 ) );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->get( 4 ) );
var_dump( $hash->add( 4, 9 ) );

echo "\ndefault value\n";
var_dump( $hash->add( 5 ) );
var_dump( $hash->get( 5 ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
without dupe checking
bool(false)
bool(false)
bool(true)
bool(true)
int(22)
bool(true)

with dupe checking
bool(false)
bool(false)
bool(true)
bool(true)
int(78)
bool(false)

default value
bool(true)
int(1)
```
