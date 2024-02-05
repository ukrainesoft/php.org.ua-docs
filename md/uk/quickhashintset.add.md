---
navigation:
  - class.quickhashintset.md: « QuickHashIntSet
  - quickhashintset.construct.md: 'QuickHashIntSet::\_\_construct »'
  - index.md: PHP Manual
  - class.quickhashintset.md: QuickHashIntSet
title: 'QuickHashIntSet::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntSet::add

(PECL quickhash >= Unknown)

QuickHashIntSet::add — Метод додає новий запис до набору

### Опис

```methodsynopsis
public QuickHashIntSet::add(int $key): bool
```

Метод додає новий запис у набір і повертає, чи був запис доданий. За умовчанням, додавання відбувається завжди, якщо під час створення хеша не використовувався прапор **`QuickHashIntSet::CHECK_FOR_DUPES`**

### Список параметрів

`key`

Ключ запису, що додається.

### Значення, що повертаються

Метод возвращает\*\*`true`\*\*, якщо запис було додано та **`false`**, якщо запис не було додано.

### Приклади

**Пример #1 Пример использования**QuickHashIntSet::add()\*\*\*\*

```php
<?php
echo "без проверки дубликатов\n";
$set = new QuickHashIntSet( 1024 );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );

echo "\nс проверкой дубликатов\n";
$set = new QuickHashIntSet( 1024, QuickHashIntSet::CHECK_FOR_DUPES );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );
var_dump( $set->exists( 4 ) );
var_dump( $set->add( 4 ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
без проверки дубликатов
bool(false)
bool(true)
bool(true)
bool(true)

с проверкой дубликатов
bool(false)
bool(true)
bool(true)
bool(false)
```
