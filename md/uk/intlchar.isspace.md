---
navigation:
  - intlchar.ispunct.md: '« IntlChar::ispunct'
  - intlchar.istitle.md: 'IntlChar::istitle »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isspace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isspace

(PHP 7, PHP 8)

IntlChar::isspace — Перевіряє, чи є символ пробельним

### Опис

```methodsynopsis
public static IntlChar::isspace(int|string $codepoint): ?bool
```

Перевіряє, чи є символ пробіл.

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є пробельним символом, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isspace("A"));
var_dump(IntlChar::isspace(" "));
var_dump(IntlChar::isspace("\n"));
var_dump(IntlChar::isspace("\t"));
var_dump(IntlChar::isspace("\u{00A0}"));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
bool(true)
bool(true)
bool(true)
```

### Дивіться також

-   [IntlChar::isJavaSpaceChar()](intlchar.isjavaspacechar.md) \- Перевірити, чи є символ пробельним з точки зору Java
-   [IntlChar::isWhitespace()](intlchar.iswhitespace.md) \- Перевірити, чи є символ пробельним з точки зору ICU
-   [IntlChar::isUWhiteSpace()](intlchar.isuwhitespace.md) \- Перевірити, чи має символ властивість White\_Space (пробіловий символ)
-   [ctype\_space()](function.ctype-space.md) \- Перевіряє пробільні символи
