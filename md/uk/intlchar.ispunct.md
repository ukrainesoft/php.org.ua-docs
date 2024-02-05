---
navigation:
  - intlchar.isprint.md: '« IntlChar::isprint'
  - intlchar.isspace.md: 'IntlChar::isspace »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::ispunct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::ispunct

(PHP 7, PHP 8)

IntlChar::ispunct — Перевіряє, чи символ символу пунктуації.

### Опис

```methodsynopsis
public static IntlChar::ispunct(int|string $codepoint): ?bool
```

Перевіряє, чи є символом пунктуації.

**`true`** для символів із категорією "P" (пунктуація).

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є символом пунктуації, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::ispunct("."));
var_dump(IntlChar::ispunct(","));
var_dump(IntlChar::ispunct("\n"));
var_dump(IntlChar::ispunct("$"));
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
bool(false)
bool(false)
```

### Дивіться також

-   [ctype\_punct()](function.ctype-punct.md) \- Перевіряє друковані символи, які не містять пробілових або буквено-цифрових символів
