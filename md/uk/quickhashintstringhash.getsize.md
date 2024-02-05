---
navigation:
  - quickhashintstringhash.get.md: '« QuickHashIntStringHash::get'
  - quickhashintstringhash.loadfromfile.md: 'QuickHashIntStringHash::loadFromFile »'
  - index.md: PHP Manual
  - class.quickhashintstringhash.md: QuickHashIntStringHash
title: 'QuickHashIntStringHash::getSize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntStringHash::getSize

(PECL quickhash >= Unknown)

QuickHashIntStringHash::getSize — Повертає кількість елементів у хеші

### Опис

```methodsynopsis
public QuickHashIntStringHash::getSize(): int
```

Повертає кількість елементів у хеші.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість елементів у хеш.

### Приклади

**Пример #1 Пример использования**QuickHashIntStringHash::getSize()\*\*\*\*

```php
<?php
$hash = new QuickHashIntStringHash( 8 );
var_dump( $hash->add( 2, "two" ) );
var_dump( $hash->add( 3, 5 ) );
var_dump( $hash->getSize() );
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
int(2)
```
