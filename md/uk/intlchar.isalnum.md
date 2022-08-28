Перевірити, чи є символ буквою чи цифрою

-   [« IntlChar::hasBinaryProperty](intlchar.hasbinaryproperty.html)
    
-   [IntlChar::isalpha »](intlchar.isalpha.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Перевірити, чи є символ буквою чи цифрою
    

# IntlChar::isalnum

(PHP 7, PHP 8)

IntlChar::isalnum — Перевірити, чи є символ буквою чи цифрою

### Опис

```methodsynopsis
public static IntlChar::isalnum(int|string $codepoint): ?bool
```

Перевіряє, чи є символ буквою чи цифрою . **`true`** категорій "L" (літери) та "Nd" (десяткові цифри).

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є буквою або цифрою, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isalnum("A"));
var_dump(IntlChar::isalnum("1"));
var_dump(IntlChar::isalnum("\u{2603}"));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(true)
bool(false)
```

### Дивіться також

-   [IntlChar::isalpha()](intlchar.isalpha.html) - Перевірити, чи є символ літерою
-   [IntlChar::isdigit()](intlchar.isdigit.html) - Перевірити, чи є символ цифрою