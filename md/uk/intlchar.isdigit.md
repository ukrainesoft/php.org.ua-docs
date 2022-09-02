---
navigation:
  - intlchar.isdefined.md: '« IntlChar::isdefined'
  - intlchar.isgraph.md: 'IntlChar::isgraph »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isdigit'
---
# IntlChar::isdigit

(PHP 7, PHP 8)

IntlChar::isdigit — Перевірити, чи символ є цифрою

### Опис

```methodsynopsis
public static IntlChar::isdigit(int|string $codepoint): ?bool
```

Перевіряє, чи символ є цифрою.

**`true`** для символів категорії "Nd" (десяткові цифри). Починаючи з Unicode 4, функція є аналогом тестування на NumericТип для Decimal.

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є цифрою, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isdigit("A"));
var_dump(IntlChar::isdigit("1"));
var_dump(IntlChar::isdigit("\t"));
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
bool(false)
```

### Дивіться також

-   [IntlChar::isalpha()](intlchar.isalpha.md) - Перевірити, чи є символ літерою
-   [IntlChar::isalnum()](intlchar.isalnum.md) - Перевірити, чи є символ буквою чи цифрою
-   [IntlChar::isxdigit()](intlchar.isxdigit.md) - Перевірити, чи є символ шістнадцятковою цифрою
