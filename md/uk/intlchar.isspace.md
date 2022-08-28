Перевіряє, чи є символ пробельним

-   [« IntlChar::ispunct](intlchar.ispunct.html)
    
-   [IntlChar::istitle »](intlchar.istitle.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Перевіряє, чи є символ пробельним
    

# IntlChar::isspace

(PHP 7, PHP 8)

IntlChar::isspace — Перевіряє, чи є символ пробельним

### Опис

```methodsynopsis
public static IntlChar::isspace(int|string $codepoint): ?bool
```

Перевіряє, чи є символ пробельним.

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є пробельним символом, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isspace("A"));
var_dump(IntlChar::isspace(" "));
var_dump(IntlChar::isspace("\n"));
var_dump(IntlChar::isspace("\t"));
var_dump(IntlChar::isspace("\u{00A0}"));
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

-   [IntlChar::isJavaSpaceChar()](intlchar.isjavaspacechar.html) - Перевірити, чи є символ пробельним з погляду мови Java
-   [IntlChar::isWhitespace()](intlchar.iswhitespace.html) - Перевірити, чи є символ пробельним з точки зору ICU
-   [IntlChar::isUWhiteSpace()](intlchar.isuwhitespace.html) - Перевірити, чи має символ властивість WhiteSpace (пробіловий символ)