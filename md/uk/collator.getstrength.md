Отримує поточну силу зіставлення

-   [« Collator::getSortKey](collator.getsortkey.html)
    
-   [Collator::setAttribute »](collator.setattribute.html)
    
-   [PHP Manual](index.html)
    
-   [Collator](class.collator.html)
    
-   Отримує поточну силу зіставлення
    

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

Об'єкт [Collator](class.collator.html)

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

-   [Константы](class.collator.html#intl.collator-constants) [Collator](class.collator.html)
-   [collator\_set\_strength()](collator.setstrength.html) - встановлює силу зіставлення
-   [collator\_get\_attribute()](collator.getattribute.html) - Отримує значення атрибуту зіставлення