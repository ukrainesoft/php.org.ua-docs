Отримує значення атрибуту зіставлення

-   [« Collator::create](collator.create.html)
    
-   [Collator::getErrorCode »](collator.geterrorcode.html)
    
-   [PHP Manual](index.html)
    
-   [Collator](class.collator.html)
    
-   Отримує значення атрибуту зіставлення
    

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

Об'єкт [Collator](class.collator.html)

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

-   [Константы](class.collator.html#intl.collator-constants) [Collator](class.collator.html)
-   [collatorsetattribute()](collator.setattribute.html) - Встановлює атрибут зіставлення
-   [collatorgetstrength()](collator.getstrength.html) - набуває поточної сили зіставлення