Отримати числову виставу для символу Unicode

-   [« IntlChar::getIntPropertyValue](intlchar.getintpropertyvalue.html)
    
-   [IntlChar::getPropertyEnum »](intlchar.getpropertyenum.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Отримати числову виставу для символу Unicode
    

# IntlChar::getNumericValue

(PHP 7, PHP 8)

IntlChar::getNumericValue — Отримати числову виставу для символу Unicode

### Опис

```methodsynopsis
public static IntlChar::getNumericValue(int|string $codepoint): ?float
```

Отримує числове уявлення символу Unicode, як у базі символів Unicode.

Якщо для символу відсутня чисельна вистава - буде повернено **`IntlChar::NO_NUMERIC_VALUE`**

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Чисельне значення `codepoint`, або **`IntlChar::NO_NUMERIC_VALUE`** якщо відсутня чи не задано. Ця константа з'явилася в PHP 7.0.6, до цієї версії у такому разі поверталося (float)`-123456789`. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::getNumericValue("4"));
var_dump(IntlChar::getNumericValue("x"));
var_dump(IntlChar::getNumericValue("\u{216C}"));
?>
```

Результат виконання цього прикладу:

```
float(4)
float(-123456789)
float(50)
```