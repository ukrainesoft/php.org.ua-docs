Перетворює символ Unicode у titlecase

-   [« IntlChar::tolower](intlchar.tolower.html)
    
-   [IntlChar::toupper »](intlchar.toupper.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Перетворює символ Unicode у titlecase
    

# IntlChar::totitle

(PHP 7, PHP 8)

IntlChar::totitle — Перетворює символ Unicode у titlecase

### Опис

```methodsynopsis
public static IntlChar::totitle(int|string $codepoint): int|string|null
```

Повертає еквівалент символу в титульному (titlecase) регістрі. Якщо немає, то повертається вихідний символ.

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає SimpleTitlecaseMapping для символу, якщо існує. Якщо ні, повертає вихідний символ. У разі виникнення помилки повертає **`null`**

Тип, що повертається повинен бути int, якщо тільки символ не був переданий як рядок UTF-8 (string), у цьому випадку повернеться рядок (string). У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::totitle("A"));
var_dump(IntlChar::totitle("a"));
var_dump(IntlChar::totitle("Φ"));
var_dump(IntlChar::totitle("φ"));
var_dump(IntlChar::totitle("1"));
var_dump(IntlChar::totitle(ord("A")));
var_dump(IntlChar::totitle(ord("a")));
?>
```

Результат виконання цього прикладу:

```
string(1) "A"
string(1) "A"
string(2) "Φ"
string(2) "Φ"
string(1) "1"
int(65)
int(65)
```

### Дивіться також

-   [IntlChar::tolower()](intlchar.tolower.html) - Перетворення символу Unicode на нижній регістр
-   [IntlChar::toupper()](intlchar.toupper.html) - Перетворення символу Unicode у верхній регістр
-   [mb\_convert\_case()](function.mb-convert-case.html) - Здійснює зміну регістру символів у рядку