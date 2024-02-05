---
navigation:
  - collator.getsortkey.md: '« Collator::getSortKey'
  - collator.setattribute.md: 'Collator::setAttribute »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::getStrength'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collator::getStrength

# collator\_get\_strength

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::getStrength -- collator\_get\_strength — Отримує поточну силу зіставлення

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Collator::getStrength(): int
```

Процедурний стиль

```methodsynopsis
collator_get_strength(Collator $object): int
```

### Список параметрів

`object`

Об'єкт [Collator](class.collator.md)

### Значення, що повертаються

Повертає поточну силу зіставлення або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**collator\_get\_strength()\*\*\*\*

```php
<?php
$coll     = collator_create( 'en_US' );
$strength = collator_get_strength( $coll );
?>
```

### Дивіться також

-   [Константи](class.collator.md#intl.collator-constants) [Collator](class.collator.md)
-   [collator\_set\_strength()](collator.setstrength.md) \- встановлює силу зіставлення
-   [collator\_get\_attribute()](collator.getattribute.md) \- Отримує значення атрибуту зіставлення
