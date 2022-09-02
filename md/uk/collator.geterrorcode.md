---
navigation:
  - collator.getattribute.md: '« Collator::getAttribute'
  - collator.geterrormessage.md: 'Collator::getErrorMessage »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::getErrorCode'
---
# Collator::getErrorCode

# collatorgeterrorcode

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::getErrorCode -- collatorgeterrorcode — Отримує останній код помилки Collator

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Collator::getErrorCode(): int|false
```

Процедурний стиль

```methodsynopsis
collator_get_error_code(Collator $object): int|false
```

### Список параметрів

`object`

Об'єкт [Collator](class.collator.md)

### Значення, що повертаються

Код помилки, повернутий останнім викликом функції API Collator або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **collatorgeterrorcode()****

```php
<?php
$coll = collator_create( 'en_US' );
if( collator_get_attribute( $coll, Collator::FRENCH_COLLATION ) === false )
        handle_error( collator_get_error_code() );
?>
```

### Дивіться також

-   [collatorgeterrormessage()](collator.geterrormessage.md) - Отримує текст для останньої помилки коду Collator
