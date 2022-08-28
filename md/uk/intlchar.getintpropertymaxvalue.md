Отримати мінімальне значення для властивості Unicode

-   [« IntlChar::getFC\_NFKC\_Closure](intlchar.getfc-nfkc-closure.html)
    
-   [IntlChar::getIntPropertyMinValue »](intlchar.getintpropertyminvalue.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Отримати мінімальне значення для властивості Unicode
    

# IntlChar::getIntPropertyMaxValue

(PHP 7, PHP 8)

IntlChar::getIntPropertyMaxValue — Отримати мінімальне значення для властивості Unicode

### Опис

```methodsynopsis
public static IntlChar::getIntPropertyMaxValue(int $property): int
```

Отримує мінімальне значення (перелічуване/цілочисленне/бінарне) для властивості Unicode.

### Список параметрів

`property`

Властивість Unicode для відображення (Дивись константи `IntlChar::PROPERTY_*`

### Значення, що повертаються

Максимальне значення, що повертається [IntlChar::getIntPropertyValue()](intlchar.getintpropertyvalue.html) для властивості Unicode . `<=0`якщо властивість не входить у допустимий діапазон.

### Приклади

**Приклад #1 Тестування різних властивостей**

```php
<?php
var_dump(IntlChar::getIntPropertyMaxValue(IntlChar::PROPERTY_BIDI_CLASS));
var_dump(IntlChar::getIntPropertyMaxValue(IntlChar::PROPERTY_SCRIPT));
var_dump(IntlChar::getIntPropertyMaxValue(IntlChar::PROPERTY_IDEOGRAPHIC));
var_dump(IntlChar::getIntPropertyMaxValue(999999999)); // Some made-up value
?>
```

Результат виконання цього прикладу:

```
int(22)
int(166)
int(1)
int(-1)
```

### Дивіться також

-   [IntlChar::hasBinaryProperty()](intlchar.hasbinaryproperty.html) - Перевірити бінарну властивість Unicode для символу
-   [IntlChar::getIntPropertyMinValue()](intlchar.getintpropertyminvalue.html) - Отримати мінімальне значення для властивості Unicode
-   [IntlChar::getIntPropertyValue()](intlchar.getintpropertyvalue.html) - Отримати значення властивості Unicode для символу
-   [IntlChar::getUnicodeVersion()](intlchar.getunicodeversion.html) - Отримати версію Unicode