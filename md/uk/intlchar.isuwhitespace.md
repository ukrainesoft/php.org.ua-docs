---
navigation:
  - intlchar.isuuppercase.md: '« IntlChar::isUUppercase'
  - intlchar.iswhitespace.md: 'IntlChar::isWhitespace »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isUWhiteSpace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isUWhiteSpace

(PHP 7, PHP 8)

IntlChar::isUWhiteSpace — Перевірити, чи має символ властивість White\_Space (пробіловий символ)

### Опис

```methodsynopsis
public static IntlChar::isUWhiteSpace(int|string $codepoint): ?bool
```

Перевіряє, чи має символ властивість White\_Space (пробіловий символ).

Те саме, що й `IntlChar::hasBinaryProperty($codepoint, IntlChar::PROPERTY_WHITE_SPACE)`

> **Зауваження** :
> 
> Відрізняється від [IntlChar::isspace()](intlchar.isspace.md) і [IntlChar::isWhitespace()](intlchar.iswhitespace.md)

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` має властивість "White\_Space", **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isUWhiteSpace("A"));
var_dump(IntlChar::isUWhiteSpace(" "));
var_dump(IntlChar::isUWhiteSpace("\n"));
var_dump(IntlChar::isUWhiteSpace("\t"));
var_dump(IntlChar::isUWhiteSpace("\u{00A0}"));
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

-   [IntlChar::isspace()](intlchar.isspace.md) \- Перевіряє, чи є символ пробельним
-   [IntlChar::isWhitespace()](intlchar.iswhitespace.md) \- Перевірити, чи є символ пробельним з точки зору ICU
-   [IntlChar::isJavaSpaceChar()](intlchar.isjavaspacechar.md) \- Перевірити, чи є символ пробельним з точки зору Java
-   [IntlChar::hasBinaryProperty()](intlchar.hasbinaryproperty.md) \- Перевірити бінарну властивість Unicode для символу
-   **`IntlChar::PROPERTY_WHITE_SPACE`**
