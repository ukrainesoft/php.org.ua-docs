---
navigation:
  - quickhashintstringhash.exists.html: '« QuickHashIntStringHash::exists'
  - quickhashintstringhash.getsize.html: 'QuickHashIntStringHash::getSize »'
  - index.html: PHP Manual
  - class.quickhashintstringhash.html: QuickHashIntStringHash
title: 'QuickHashIntStringHash::get'
---
# QuickHashIntStringHash::get

(PECL quickhash >= Unknown)

QuickHashIntStringHash::get — Метод витягує значення з хеша за його ключем

### Опис

```methodsynopsis
public QuickHashIntStringHash::get(int $key): mixed
```

Метод отримує значення з хеша за його ключем.

### Список параметрів

`key`

Ключ одержуваного запису.

### Значення, що повертаються

Метод повертає значення, якщо ключ існує або \*\*`null`\*\*якщо ключ не є частиною хеша.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntStringHash::get()****

```php
<?php
$hash = new QuickHashIntStringHash( 8 );
var_dump( $hash->get( 1 ) );

var_dump( $hash->add( 2, "two" ) );
var_dump( $hash->get( 2 ) );

var_dump( $hash->add( 3, 5 ) );
var_dump( $hash->get( 3 ) );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
string(3) "two"
bool(true)
string(1) "5"
```
