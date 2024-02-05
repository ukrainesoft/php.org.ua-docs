---
navigation:
  - intlchar.istitle.md: '« IntlChar::istitle'
  - intlchar.isulowercase.md: 'IntlChar::isULowercase »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isUAlphabetic'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isUAlphabetic

(PHP 7, PHP 8)

IntlChar::isUAlphabetic — Перевірити, чи встановлено у символу властивість Alphabetic

### Опис

```methodsynopsis
public static IntlChar::isUAlphabetic(int|string $codepoint): ?bool
```

Перевіряє, чи встановлено символ символу Alphabetic.

Те саме, що і `IntlChar::hasBinaryProperty($codepoint, IntlChar::PROPERTY_ALPHABETIC)`

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint`имеет свойство Alphabetic,**`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isUAlphabetic("A"));
var_dump(IntlChar::isUAlphabetic("1"));
var_dump(IntlChar::isUAlphabetic("\u{2603}"));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
bool(false)
```

### Дивіться також

-   [IntlChar::isalpha()](intlchar.isalpha.md) \- Перевірити, чи є символ літерою
-   [IntlChar::hasBinaryProperty()](intlchar.hasbinaryproperty.md) \- Перевірити бінарну властивість Unicode для символу
-   **`IntlChar::PROPERTY_ALPHABETIC`**
