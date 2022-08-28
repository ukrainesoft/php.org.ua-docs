Створює новий екземпляр Collator

-   [« Collator::\_\_construct](collator.construct.html)
    
-   [Collator::getAttribute »](collator.getattribute.html)
    
-   [PHP Manual](index.html)
    
-   [Collator](class.collator.html)
    
-   Створює новий екземпляр Collator
    

# Collator::create

# collatorcreate

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::create -- collatorcreate — Створює новий екземпляр Collator

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Collator::create(string $locale): ?Collator
```

Процедурний стиль

```methodsynopsis
collator_create(string $locale): ?Collator
```

Рядки будуть порівнюватися з використанням зазначених параметрів.

### Список параметрів

`locale`

Локаль, що містить необхідні правила зіставлення. Можуть бути передані спеціальні значення для мовних стандартів, якщо для мовного стандарту передано порожній рядок (string), будуть використовуватися правила зіставлення мовних стандартів за промовчанням. Якщо передається значення `"root"`, використовуватимуться правила [» UCA](http://www.unicode.org/reports/tr10/)

### Значення, що повертаються

Повертає новий екземпляр [Collator](class.collator.html) або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **collatorcreate()****

```php
<?php
$coll = collator_create( 'en_US' );

if( !isset( $coll ) ) {
    printf( "Не удалось создать Collator: %s\n", intl_get_error_message() );
    exit( 1 );
}
?>
```

### Дивіться також

-   [Collator::\_\_construct()](collator.construct.html) - Створює новий екземпляр Collator