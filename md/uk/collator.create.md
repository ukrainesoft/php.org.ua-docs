---
navigation:
  - collator.construct.md: '« Collator::\_\_construct'
  - collator.getattribute.md: 'Collator::getAttribute »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::create'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collator::create

# collator\_create

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::create -- collator\_create — Створює новий екземпляр Collator

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

Локаль, що містить необхідні правила зіставлення. Можуть бути передані спеціальні значення для мовних стандартів, якщо для мовного стандарту передано порожній рядок (string), будуть використовуватися правила зіставлення мовних стандартів за промовчанням. Якщо передається значення `"root"`, будут использоваться правила[» UCA](https://www.unicode.org/reports/tr10/)

### Значення, що повертаються

Повертає новий екземпляр [Collator](class.collator.md)или\*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**collator\_create()\*\*\*\*

```php
<?php
$coll = collator_create( 'en_US' );

if( !isset( $coll ) ) {
    printf( "Не удалось создать Collator: %s\n", intl_get_error_message() );
    exit( 1 );
}
?>
```

### Дивіться також

-   [Collator::\_\_construct()](collator.construct.md) \- Створює новий екземпляр Collator
