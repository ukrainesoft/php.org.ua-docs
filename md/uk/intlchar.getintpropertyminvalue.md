Отримати мінімальне значення для властивості Unicode

-   [« IntlChar::getIntPropertyMaxValue](intlchar.getintpropertymaxvalue.html)
    
-   [IntlChar::getIntPropertyValue »](intlchar.getintpropertyvalue.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Отримати мінімальне значення для властивості Unicode
    

# IntlChar::getIntPropertyMinValue

(PHP 7, PHP 8)

IntlChar::getIntPropertyMinValue — Отримати мінімальне значення для властивості Unicode

### Опис

```methodsynopsis
public static IntlChar::getIntPropertyMinValue(int $property): int
```

Отримує мінімальне значення (перелічуване/цілочисленне/бінарне) для властивості Unicode.

### Список параметрів

`property`

Властивість Unicode для відображення (Дивись константи `IntlChar::PROPERTY_*`

### Значення, що повертаються

Мінімальне значення, що повертається [IntlChar::getIntPropertyValue()](intlchar.getintpropertyvalue.html) для властивості Unicode . `0`якщо властивість не входить у допустимий діапазон.

### Приклади

**Приклад #1 Тестування різних властивостей**

```php
<?php
var_dump(IntlChar::getIntPropertyMinValue(IntlChar::PROPERTY_BIDI_CLASS));
var_dump(IntlChar::getIntPropertyMinValue(IntlChar::PROPERTY_SCRIPT));
var_dump(IntlChar::getIntPropertyMinValue(IntlChar::PROPERTY_IDEOGRAPHIC));
var_dump(IntlChar::getIntPropertyMinValue(999999999)); // Some made-up value
?>
```

Результат виконання цього прикладу:

```
int(0)
int(0)
int(0)
int(0)
```

### Дивіться також

-   [IntlChar::hasBinaryProperty()](intlchar.hasbinaryproperty.html) - Перевірити бінарну властивість Unicode для символу
-   [IntlChar::getIntPropertyMaxValue()](intlchar.getintpropertymaxvalue.html) - Отримати мінімальне значення для властивості Unicode
-   [IntlChar::getIntPropertyValue()](intlchar.getintpropertyvalue.html) - Отримати значення властивості Unicode для символу
-   [IntlChar::getUnicodeVersion()](intlchar.getunicodeversion.html) - Отримати версію Unicode