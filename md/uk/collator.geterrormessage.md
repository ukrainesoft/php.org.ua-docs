Отримує текст для останньої помилки коду Collator

-   [« Collator::getErrorCode](collator.geterrorcode.md)
    
-   [Collator::getLocale »](collator.getlocale.md)
    
-   [PHP Manual](index.md)
    
-   [Collator](class.collator.md)
    
-   Отримує текст для останньої помилки коду Collator
    

# Collator::getErrorMessage

# collatorgeterrormessage

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::getErrorMessage -- collatorgeterrormessage — Отримує текст для останньої помилки коду Collator

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

Опис помилки, повернутий останнім викликом функції API Collator або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **collatorgeterrormessage()****

```php
<?php
$coll = collator_create( 'lt' );
if( collator_compare( $coll, 'y', 'k' ) === false ) {
    echo collator_get_error_message( $coll );
}
?>
```

### Дивіться також

-   [collatorgeterrorcode()](collator.geterrorcode.md) - Отримує останній код помилки Collator