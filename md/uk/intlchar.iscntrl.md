Перевірити, чи є символ керуючим

-   [« IntlChar::isblank](intlchar.isblank.html)
    
-   [IntlChar::isdefined »](intlchar.isdefined.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Перевірити, чи є символ керуючим
    

# IntlChar::iscntrl

(PHP 7, PHP 8)

IntlChar::iscntrl — Перевірити, чи є символ керуючим

### Опис

```methodsynopsis
public static IntlChar::iscntrl(int|string $codepoint): ?bool
```

Перевіряє, чи є символ керуючим.

Керуючі символи:

-   8-бітові керуючі символи ISO (U+0000..U+001f та U+007f..U+009f)
-   **`IntlChar::CHAR_CATEGORY_CONTROL_CHAR`** (Cc)
-   **`IntlChar::CHAR_CATEGORY_FORMAT_CHAR`** (Cf)
-   **`IntlChar::CHAR_CATEGORY_LINE_SEPARATOR`** (Zl)
-   **`IntlChar::CHAR_CATEGORY_PARAGRAPH_SEPARATOR`** (Zp)

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є керуючим, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::iscntrl("A"));
var_dump(IntlChar::iscntrl(" "));
var_dump(IntlChar::iscntrl("\n"));
var_dump(IntlChar::iscntrl("\u{200e}"));
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(false)
bool(true)
bool(true)
```

### Дивіться також

-   [IntlChar::isprint()](intlchar.isprint.html) - Перевіряє, чи символ відображається
-   **`IntlChar::PROPERTY_DEFAULT_IGNORABLE_CODE_POINT`**