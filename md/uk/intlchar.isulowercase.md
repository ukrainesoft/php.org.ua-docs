---
navigation:
  - intlchar.isualphabetic.md: '« IntlChar::isUAlphabetic'
  - intlchar.isupper.md: 'IntlChar::isupper »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isULowercase'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isULowercase

(PHP 7, PHP 8)

IntlChar::isULowercase — Перевірити, чи символ символу в нижньому регістрі

### Опис

```methodsynopsis
public static IntlChar::isULowercase(int|string $codepoint): ?bool
```

Перевіряє, чи символ є символом у нижньому регістрі.

Те саме, що й `IntlChar::hasBinaryProperty($codepoint, IntlChar::PROPERTY_LOWERCASE)`

> **Зауваження** :
> 
> Відрізняється від [IntlChar::islower()](intlchar.islower.md) і повертає **`true`** для більшої кількості символів.

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` має властивість "Lowercase", **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isULowercase("A"));
var_dump(IntlChar::isULowercase("a"));
var_dump(IntlChar::isULowercase("Φ"));
var_dump(IntlChar::isULowercase("φ"));
var_dump(IntlChar::isULowercase("1"));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
bool(false)
bool(true)
bool(false)
```

### Дивіться також

-   [IntlChar::islower()](intlchar.islower.md) \- Перевірити, чи в нижньому регістрі символ
-   [IntlChar::hasBinaryProperty()](intlchar.hasbinaryproperty.md) \- Перевірити бінарну властивість Unicode для символу
-   **`IntlChar::PROPERTY_LOWERCASE`**
