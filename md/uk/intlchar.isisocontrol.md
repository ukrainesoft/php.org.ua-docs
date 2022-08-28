Перевірити, чи є символ керуючим відповідно до ISO

-   [« IntlChar::isIDStart](intlchar.isidstart.html)
    
-   [IntlChar::isJavaIDPart »](intlchar.isjavaidpart.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Перевірити, чи є символ керуючим відповідно до ISO
    

# IntlChar::isISOControl

(PHP 7, PHP 8)

IntlChar::isISOControl — Перевірити, чи є символ керуючим відповідно до ISO

### Опис

```methodsynopsis
public static IntlChar::isISOControl(int|string $codepoint): ?bool
```

Перевіряє, чи є символ керуючим відповідно до ISO.

**`true`** для U+0000..U+001f та U+007f..U+009f (категорія "Cc").

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є керуючим символом ISO, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isISOControl(" "));
var_dump(IntlChar::isISOControl("\n"));
var_dump(IntlChar::isISOControl("\u{200e}"));
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
bool(false)
```

### Дивіться також

-   [IntlChar::iscntrl()](intlchar.iscntrl.html) - Перевірити, чи є символ керуючим