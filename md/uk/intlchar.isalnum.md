---
navigation:
  - intlchar.hasbinaryproperty.md: '« IntlChar::hasBinaryProperty'
  - intlchar.isalpha.md: 'IntlChar::isalpha »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isalnum'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

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

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
bool(false)
```

### Дивіться також

-   [IntlChar::isalpha()](intlchar.isalpha.md) \- Перевірити, чи є символ літерою
-   [IntlChar::isdigit()](intlchar.isdigit.md) \- Перевірити, чи є символ цифрою
-   [ctype\_alnum()](function.ctype-alnum.md) \- Перевіряє буквено-цифрові символи
