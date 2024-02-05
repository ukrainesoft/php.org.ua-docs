---
navigation:
  - intlchar.isjavaidstart.md: '« IntlChar::isJavaIDStart'
  - intlchar.islower.md: 'IntlChar::islower »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isJavaSpaceChar'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isJavaSpaceChar

(PHP 7, PHP 8)

IntlChar::isJavaSpaceChar — Перевірити, чи є символ пробельним з точки зору мови Java

### Опис

```methodsynopsis
public static IntlChar::isJavaSpaceChar(int|string $codepoint): ?bool
```

Перевіряє, чи є символ пробельним з погляду мови Java.

**`true`** для категорії "Z" (розділювачі), не включаючи контрольні символи (наприклад, TAB або Переклад Рядки).

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є пробельним в Java, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isJavaSpaceChar("A"));
var_dump(IntlChar::isJavaSpaceChar(" "));
var_dump(IntlChar::isJavaSpaceChar("\n"));
var_dump(IntlChar::isJavaSpaceChar("\t"));
var_dump(IntlChar::isJavaSpaceChar("\u{00A0}"));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
bool(false)
bool(false)
bool(true)
```

### Дивіться також

-   [IntlChar::isspace()](intlchar.isspace.md) \- Перевіряє, чи є символ пробельним
-   [IntlChar::isWhitespace()](intlchar.iswhitespace.md) \- Перевірити, чи є символ пробельним з точки зору ICU
-   [IntlChar::isUWhiteSpace()](intlchar.isuwhitespace.md) \- Перевірити, чи має символ властивість White\_Space (пробіловий символ)
