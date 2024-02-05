---
navigation:
  - intlchar.isupper.md: '« IntlChar::isupper'
  - intlchar.isuwhitespace.md: 'IntlChar::isUWhiteSpace »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isUUppercase'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isUUppercase

(PHP 7, PHP 8)

IntlChar::isUUppercase — Перевірити, чи символ є символом у верхньому регістрі

### Опис

```methodsynopsis
public static IntlChar::isUUppercase(int|string $codepoint): ?bool
```

Перевірити, чи символ є символом у верхньому регістрі.

Те саме, що й `IntlChar::hasBinaryProperty($codepoint, IntlChar::PROPERTY_UPPERCASE)`

> **Зауваження** :
> 
> Відрізняється від [IntlChar::isupper()](intlchar.isupper.md) і повертає **`true`** для більшої кількості символів.

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` має властивість "Uppercase", **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isUUppercase("A"));
var_dump(IntlChar::isUUppercase("a"));
var_dump(IntlChar::isUUppercase("Φ"));
var_dump(IntlChar::isUUppercase("φ"));
var_dump(IntlChar::isUUppercase("1"));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
bool(true)
bool(false)
bool(false)
```

### Дивіться також

-   [IntlChar::isupper()](intlchar.isupper.md) - Перевірити, чи входить символ у категорію "Lu" (літера у верхньому регістрі)
-   [IntlChar::hasBinaryProperty()](intlchar.hasbinaryproperty.md) \- Перевірити бінарну властивість Unicode для символу
-   **`IntlChar::PROPERTY_UPPERCASE`**
