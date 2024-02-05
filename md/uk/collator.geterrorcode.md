---
navigation:
  - collator.getattribute.md: '« Collator::getAttribute'
  - collator.geterrormessage.md: 'Collator::getErrorMessage »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::getErrorCode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collator::getErrorCode

# collator\_get\_error\_code

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::getErrorCode -- collator\_get\_error\_code — Отримує останній код помилки Collator

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

Код помилки, повернутий останнім викликом функції API Collator або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** collator\_get\_error\_code()\*\*\*\*

```php
<?php
$coll = collator_create( 'en_US' );
if( collator_get_attribute( $coll, Collator::FRENCH_COLLATION ) === false )
        handle_error( collator_get_error_code() );
?>
```

### Дивіться також

-   [collator\_get\_error\_message()](collator.geterrormessage.md) \- Отримує текст для останньої помилки коду Collator
