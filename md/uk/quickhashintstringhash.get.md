---
navigation:
  - quickhashintstringhash.exists.md: '« QuickHashIntStringHash::exists'
  - quickhashintstringhash.getsize.md: 'QuickHashIntStringHash::getSize »'
  - index.md: PHP Manual
  - class.quickhashintstringhash.md: QuickHashIntStringHash
title: 'QuickHashIntStringHash::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Приклад #1 Приклад використання** QuickHashIntStringHash::get()\*\*\*\*

```php
<?php
$hash = new QuickHashIntStringHash( 8 );
var_dump( $hash->get( 1 ) );

var_dump( $hash->add( 2, "two" ) );
var_dump( $hash->get( 2 ) );

var_dump( $hash->add( 3, 5 ) );
var_dump( $hash->get( 3 ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
string(3) "two"
bool(true)
string(1) "5"
```
