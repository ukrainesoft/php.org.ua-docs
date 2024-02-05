---
navigation:
  - intlchar.isalnum.md: '« IntlChar::isalnum'
  - intlchar.isbase.md: 'IntlChar::isbase »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isalpha'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isalpha

(PHP 7, PHP 8)

IntlChar::isalpha — Перевірити, чи є символ літерою

### Опис

```methodsynopsis
public static IntlChar::isalpha(int|string $codepoint): ?bool
```

Перевіряє, чи є символ літерою . **`true`** для категорії "L" (літери).

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є буквою, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isalpha("A"));
var_dump(IntlChar::isalpha("1"));
var_dump(IntlChar::isalpha("\u{2603}"));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
bool(false)
```

### Дивіться також

-   [IntlChar::isalnum()](intlchar.isalnum.md) \- Перевірити, чи є символ буквою чи цифрою
-   [IntlChar::isdigit()](intlchar.isdigit.md) \- Перевірити, чи є символ цифрою
-   [ctype\_alpha()](function.ctype-alpha.md) \- Перевіряє буквені символи
