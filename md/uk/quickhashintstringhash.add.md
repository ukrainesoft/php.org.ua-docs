---
navigation:
  - class.quickhashintstringhash.md: « QuickHashIntStringHash
  - quickhashintstringhash.construct.md: 'QuickHashIntStringHash::\_\_construct »'
  - index.md: PHP Manual
  - class.quickhashintstringhash.md: QuickHashIntStringHash
title: 'QuickHashIntStringHash::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntStringHash::add

(PECL quickhash >= Unknown)

QuickHashIntStringHash::add — Метод додає новий запис у хеш

### Опис

```methodsynopsis
public QuickHashIntStringHash::add(int $key, string $value): bool
```

Метод додає новий запис у набір і повертає, чи був запис доданий. За умовчанням, додавання відбувається завжди, якщо під час створення хеша не використовувався прапор **`QuickHashIntStringHash::CHECK_FOR_DUPES`**

### Список параметрів

`key`

Ключ запису, що додається.

`value`

Значення запису, що додається. Якщо передається нестрокове значення, воно буде автоматично перетворено на рядок, якщо це можливо.

### Значення, що повертаються

Метод возвращает\*\*`true`\*\*, якщо запис було додано та **`false`**, якщо запис не було додано.

### Приклади

**Приклад #1 Приклад використання** QuickHashIntStringHash::add()\*\*\*\*

```php
<?php
echo "без проверки дубликатов\n";
$hash = new QuickHashIntStringHash( 1024 );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->get( 4 ) );
var_dump( $hash->add( 4, "twenty two" ) );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->get( 4 ) );
var_dump( $hash->add( 4, "twelve" ) );

echo "\nс проверкой дубликатов\n";
$hash = new QuickHashIntStringHash( 1024, QuickHashIntStringHash::CHECK_FOR_DUPES );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->get( 4 ) );
var_dump( $hash->add( 4, "seventy eight" ) );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->get( 4 ) );
var_dump( $hash->add( 4, "nine" ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
без проверки дубликатов
bool(false)
bool(false)
bool(true)
bool(true)
string(10) "twenty two"
bool(true)

с проверкой дубликатов
bool(false)
bool(false)
bool(true)
bool(true)
string(13) "seventy eight"
bool(false)
```
