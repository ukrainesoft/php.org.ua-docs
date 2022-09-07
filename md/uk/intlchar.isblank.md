---
navigation:
  - intlchar.isbase.md: '« IntlChar::isbase'
  - intlchar.iscntrl.md: 'IntlChar::iscntrl »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isblank'
---
# IntlChar::isblank

(PHP 7, PHP 8)

IntlChar::isblank — Перевірити, чи є символ "порожнім" або "горизонтальним пропуском"

### Опис

```methodsynopsis
public static IntlChar::isblank(int|string $codepoint): ?bool
```

Перевіряє, чи є символ "порожнім" чи "горизонтальним пропуском". Тобто. символ візуально розділяє слова в реченні.

Іншими словами:

-   **`true`** для пробільних символів Unicode за винятком "вертикальних символів пробілів", таких як: U+000A (LF) U+000B (VT) U+000C (FF) U+000D (CR) U+0085 (NEL) U+2028 (LS ) U+2029 (PS)
-   **`true`** для U+0009 (TAB) та символів із категорії "Zs" (пробільні роздільники) за винятком пробілу з нульовою довжиною (ZWSP, U+200B).

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є "порожнім" чи "горизонтальним пропуском", **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isblank("A"));
var_dump(IntlChar::isblank(" "));
var_dump(IntlChar::isblank("\t"));
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
bool(true)
```

### Дивіться також

-   [IntlChar::isspace()](intlchar.isspace.md) - Перевіряє, чи є символ пробельним
-   [IntlChar::isJavaSpaceChar()](intlchar.isjavaspacechar.md) - Перевірити, чи є символ пробельним з точки зору Java
-   [IntlChar::isUWhiteSpace()](intlchar.isuwhitespace.md) - Перевірити, чи має символ властивість WhiteSpace (пробіловий символ)
-   [IntlChar::isWhitespace()](intlchar.iswhitespace.md) - Перевірити, чи є символ пробельним з точки зору ICU
