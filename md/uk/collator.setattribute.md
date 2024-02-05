---
navigation:
  - collator.getstrength.md: '« Collator::getStrength'
  - collator.setstrength.md: 'Collator::setStrength »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::setAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collator::setAttribute

# collator\_set\_attribute

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::setAttribute -- collator\_set\_attribute - Встановлює атрибут зіставлення

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Collator::setAttribute(int $attribute, int $value): bool
```

Процедурний стиль

```methodsynopsis
collator_set_attribute(Collator $object, int $attribute, int $value): bool
```

### Список параметрів

`object`

Об'єкт [Collator](class.collator.md)

`attribute`

Атрибут.

`value`

Значення атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**collator\_set\_attribute()\*\*\*\*

```php
<?php
$coll = collator_create( 'en_CA' );
$val  = collator_get_attribute( $coll, Collator::NUMERIC_COLLATION );
if ($val === false) {
    // Обработка ошибки.
} elseif ($val === Collator::ON) {
    // Делаем что-то полезное.
}
?>
```

### Дивіться також

-   [Константи](class.collator.md#intl.collator-constants) [Collator](class.collator.md)
-   [collator\_get\_attribute()](collator.getattribute.md) \- Отримує значення атрибуту зіставлення
-   [collator\_set\_strength()](collator.setstrength.md) \- встановлює силу зіставлення
