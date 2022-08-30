Отримати код символ Unicode

-   [« IntlChar::isxdigit](intlchar.isxdigit.html)
    
-   [IntlChar::tolower »](intlchar.tolower.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Отримати код символ Unicode
    

# IntlChar::ord

(PHP 7, PHP 8)

IntlChar::ord — Отримати код Unicode

### Опис

```methodsynopsis
public static IntlChar::ord(int|string $character): ?int
```

Повертає код Unicode.

Ця функція протилежна дії функції [IntlChar::chr()](intlchar.chr.html)

### Список параметрів

`character`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає код Unicode у вигляді цілого числа.

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::ord("A"));
var_dump(IntlChar::ord(" "));
var_dump(IntlChar::ord("\u{2603}"));
?>
```

Результат виконання цього прикладу:

```
int(65)
int(32)
int(9731)
```

### Дивіться також

-   [IntlChar::chr()](intlchar.chr.html) - Отримати символ Unicode за його кодом
-   [мбord()](function.mb-ord.html) - Отримує кодову точку символу Unicode
-   [ord()](function.ord.html) - Конвертує перший байт рядка до числа від 0 до 255