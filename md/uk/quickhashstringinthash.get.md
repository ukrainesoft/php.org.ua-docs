---
navigation:
  - quickhashstringinthash.exists.md: '« QuickHashStringIntHash::exists'
  - quickhashstringinthash.getsize.md: 'QuickHashStringIntHash::getSize »'
  - index.md: PHP Manual
  - class.quickhashstringinthash.md: QuickHashStringIntHash
title: 'QuickHashStringIntHash::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashStringIntHash::get

(No version information available, might only be in Git)

QuickHashStringIntHash::get — Метод витягує значення з хеша за його ключем

### Опис

```methodsynopsis
public QuickHashStringIntHash::get(string $key): mixed
```

Метод отримує значення з хеша за його ключем.

### Список параметрів

`key`

Ключ одержуваного запису.

### Значення, що повертаються

Метод повертає значення, якщо ключ існує або \*\*`null`\*\*якщо ключ не є частиною хеша.

### Приклади

**Пример #1 Пример использования**QuickHashStringIntHash::get()\*\*\*\*

```php
<?php
$hash = new QuickHashStringIntHash( 8 );
var_dump( $hash->get( "one" ) );

var_dump( $hash->add( "two", 2 ) );
var_dump( $hash->get( "two" ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
int(2)
```
