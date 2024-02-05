---
navigation:
  - quickhashinthash.exists.md: '« QuickHashIntHash::exists'
  - quickhashinthash.getsize.md: 'QuickHashIntHash::getSize »'
  - index.md: PHP Manual
  - class.quickhashinthash.md: QuickHashIntHash
title: 'QuickHashIntHash::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntHash::get

(PECL quickhash >= Unknown)

QuickHashIntHash::get — Метод витягує значення з хеша за його ключем

### Опис

```methodsynopsis
public QuickHashIntHash::get(int $key): int
```

Метод отримує значення з хеша за його ключем.

### Список параметрів

`key`

Ключ одержуваного запису.

### Значення, що повертаються

Метод повертає значення, якщо ключ існує або \*\*`null`\*\*якщо ключ не був частиною хеша.

### Приклади

**Приклад #1 Приклад використання** QuickHashIntHash::get()\*\*\*\*

```php
<?php
$hash = new QuickHashIntHash( 8 );
var_dump( $hash->get( 1 ) );

var_dump( $hash->add( 2 ) );
var_dump( $hash->get( 2 ) );

var_dump( $hash->add( 3, 5 ) );
var_dump( $hash->get( 3 ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
int(1)
bool(true)
int(5)
```
