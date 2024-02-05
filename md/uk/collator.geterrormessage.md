---
navigation:
  - collator.geterrorcode.md: '« Collator::getErrorCode'
  - collator.getlocale.md: 'Collator::getLocale »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::getErrorMessage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collator::getErrorMessage

# collator\_get\_error\_message

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::getErrorMessage -- collator\_get\_error\_message — Отримує текст для останньої помилки коду Collator

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Collator::getErrorMessage(): string|false
```

Процедурний стиль

```methodsynopsis
collator_get_error_message(Collator $object): string|false
```

Отримує повідомлення про останню помилку.

### Список параметрів

`object`

Об'єкт [Collator](class.collator.md)

### Значення, що повертаються

Опис помилки, повернутий останнім викликом функції API Collator або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** collator\_get\_error\_message()\*\*\*\*

```php
<?php
$coll = collator_create( 'lt' );
if( collator_compare( $coll, 'y', 'k' ) === false ) {
    echo collator_get_error_message( $coll );
}
?>
```

### Дивіться також

-   [collator\_get\_error\_code()](collator.geterrorcode.md) \- Отримує останній код помилки Collator
