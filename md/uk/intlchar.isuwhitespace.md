Перевірити, чи має символ властивості WhiteSpace (пробіловий символ)

-   [« IntlChar::isUUppercase](intlchar.isuuppercase.html)
    
-   [IntlChar::isWhitespace »](intlchar.iswhitespace.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Перевірити, чи має символ властивості WhiteSpace (пробіловий символ)
    

# IntlChar::isUWhiteSpace

(PHP 7, PHP 8)

IntlChar::isUWhiteSpace — Перевірити, чи має символ властивість WhiteSpace (пробіловий символ)

### Опис

```methodsynopsis
public static IntlChar::isUWhiteSpace(int|string $codepoint): ?bool
```

Перевіряє, чи має символ властивість WhiteSpace (пробіловий символ).

Те саме, що й `IntlChar::hasBinaryProperty($codepoint, IntlChar::PROPERTY_WHITE_SPACE)`

> **Зауваження**
> 
> Відрізняється від [IntlChar::isspace()](intlchar.isspace.html) і [IntlChar::isWhitespace()](intlchar.iswhitespace.html)

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` має властивість "WhiteSpace", **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isUWhiteSpace("A"));
var_dump(IntlChar::isUWhiteSpace(" "));
var_dump(IntlChar::isUWhiteSpace("\n"));
var_dump(IntlChar::isUWhiteSpace("\t"));
var_dump(IntlChar::isUWhiteSpace("\u{00A0}"));
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
bool(true)
bool(true)
bool(true)
```

### Дивіться також

-   [IntlChar::isspace()](intlchar.isspace.html) - Перевіряє, чи є символ пробельним
-   [IntlChar::isWhitespace()](intlchar.iswhitespace.html) - Перевірити, чи є символ пробельним з точки зору ICU
-   [IntlChar::isJavaSpaceChar()](intlchar.isjavaspacechar.html) - Перевірити, чи є символ пробельним з точки зору Java
-   [IntlChar::hasBinaryProperty()](intlchar.hasbinaryproperty.html) - Перевірити бінарну властивість Unicode для символу
-   **`IntlChar::PROPERTY_WHITE_SPACE`**