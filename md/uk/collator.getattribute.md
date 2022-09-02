---
navigation:
  - collator.create.md: '« Collator::create'
  - collator.geterrorcode.md: 'Collator::getErrorCode »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::getAttribute'
---
# Collator::getAttribute

# collatorgetattribute

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::getAttribute -- collatorgetattribute — Отримує значення атрибуту зіставлення

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

Значення атрибуту або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **collatorgetattribute()****

```php
<?php
$coll = collator_create( 'en_CA' );
$val = collator_get_attribute( $coll, Collator::NUMERIC_COLLATION );
if( $val === false )
{
    // Обработка ошибки
}
?>
```

### Дивіться також

-   [Константи](class.collator.md#intl.collator-constants) [Collator](class.collator.md)
-   [collatorsetattribute()](collator.setattribute.md) - Встановлює атрибут зіставлення
-   [collatorgetstrength()](collator.getstrength.md) - набуває поточної сили зіставлення
