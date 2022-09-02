---
navigation:
  - collator.getsortkey.md: '« Collator::getSortKey'
  - collator.setattribute.md: 'Collator::setAttribute »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::getStrength'
---
# Collator::getStrength

# collatorgetstrength

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::getStrength -- collatorgetstrength — Отримує поточну силу зіставлення

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

Повертає поточну силу зіставлення або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **collatorgetstrength()****

```php
<?php
$coll     = collator_create( 'en_US' );
$strength = collator_get_strength( $coll );
?>
```

### Дивіться також

-   [Константи](class.collator.md#intl.collator-constants) [Collator](class.collator.md)
-   [collatorsetstrength()](collator.setstrength.md) - встановлює силу зіставлення
-   [collatorgetattribute()](collator.getattribute.md) - Отримує значення атрибуту зіставлення
