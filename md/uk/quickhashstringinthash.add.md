---
navigation:
  - class.quickhashstringinthash.md: « QuickHashStringIntHash
  - quickhashstringinthash.construct.md: 'QuickHashStringIntHash::\_\_construct »'
  - index.md: PHP Manual
  - class.quickhashstringinthash.md: QuickHashStringIntHash
title: 'QuickHashStringIntHash::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashStringIntHash::add

(No version information available, might only be in Git)

QuickHashStringIntHash::add — Метод додає новий запис у хеш

### Опис

```methodsynopsis
public QuickHashStringIntHash::add(string $key, int $value): bool
```

Метод додає новий запис у хеш і повертає, чи був запис доданий. За умовчанням, додавання відбувається завжди, якщо під час створення хеша не використовувався прапор **`QuickHashStringIntHash::CHECK_FOR_DUPES`**

### Список параметрів

`key`

Ключ запису, що додається.

`value`

Значення запису, що додається.

### Значення, що повертаються

Метод возвращает\*\*`true`\*\*, якщо запис було додано та **`false`**, якщо запис не було додано.

### Приклади

**Приклад #1 Приклад використання** QuickHashStringIntHash::add()\*\*\*\*

```php
<?php
echo "без проверки дубликатов\n";
$hash = new QuickHashStringIntHash( 1024 );
var_dump( $hash );
var_dump( $hash->exists( "four" ) );
var_dump( $hash->get( "four" ) );
var_dump( $hash->add( "four", 22 ) );
var_dump( $hash->exists( "four" ) );
var_dump( $hash->get( "four" ) );
var_dump( $hash->add( "four", 12 ) );

echo "\nс проверкой дубликатов\n";
$hash = new QuickHashStringIntHash( 1024, QuickHashStringIntHash::CHECK_FOR_DUPES );
var_dump( $hash );
var_dump( $hash->exists( "four" ) );
var_dump( $hash->get( "four" ) );
var_dump( $hash->add( "four", 78 ) );
var_dump( $hash->exists( "four" ) );
var_dump( $hash->get( "four" ) );
var_dump( $hash->add( "four", 9 ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
без проверки дубликатов
object(QuickHashStringIntHash)#1 (0) {
}
bool(false)
bool(false)
bool(true)
bool(true)
int(22)
bool(true)

с проверкой дубликатов
object(QuickHashStringIntHash)#2 (0) {
}
bool(false)
bool(false)
bool(true)
bool(true)
int(78)
bool(false)
```
