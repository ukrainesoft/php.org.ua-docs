---
navigation:
  - collator.create.md: '« Collator::create'
  - collator.geterrorcode.md: 'Collator::getErrorCode »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::getAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collator::getAttribute

# collator\_get\_attribute

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::getAttribute -- collator\_get\_attribute — Отримує значення атрибуту зіставлення

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Collator::getAttribute(int $attribute): int|false
```

Процедурний стиль

```methodsynopsis
collator_get_attribute(Collator $object, int $attribute): int|false
```

Отримує значення цілісного атрибуту зіставника.

### Список параметрів

`object`

Об'єкт [Collator](class.collator.md)

`attribute`

Атрибут, котрому потрібно отримати значення.

### Значення, що повертаються

Значение атрибута или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**collator\_get\_attribute()\*\*\*\*

```php
<?php
$coll = collator_create( 'en_CA' );
$val = collator_get_attribute( $coll, Collator::NUMERIC_COLLATION );
if( $val === false )
{
    // Обработка ошибки
}
?>
```

### Дивіться також

-   [Константи](class.collator.md#intl.collator-constants) [Collator](class.collator.md)
-   [collator\_set\_attribute()](collator.setattribute.md) \- Встановлює атрибут зіставлення
-   [collator\_get\_strength()](collator.getstrength.md) \- набуває поточної сили зіставлення
