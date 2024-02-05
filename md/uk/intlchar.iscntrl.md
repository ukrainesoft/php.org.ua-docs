---
navigation:
  - intlchar.isblank.md: '« IntlChar::isblank'
  - intlchar.isdefined.md: 'IntlChar::isdefined »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::iscntrl'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::iscntrl

(PHP 7, PHP 8)

IntlChar::iscntrl — Перевірити, чи є символ керуючим

### Опис

```methodsynopsis
public static IntlChar::iscntrl(int|string $codepoint): ?bool
```

Перевіряє, чи є символ керуючим.

Керуючі символи:

-   8-бітові керуючі символи ISO (U+0000..U+001f та U+007f..U+009f)
-   **`IntlChar::CHAR_CATEGORY_CONTROL_CHAR`**(Cc)
-   **`IntlChar::CHAR_CATEGORY_FORMAT_CHAR`**(Cf)
-   **`IntlChar::CHAR_CATEGORY_LINE_SEPARATOR`**(Zl)
-   **`IntlChar::CHAR_CATEGORY_PARAGRAPH_SEPARATOR`**(Zp)

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint`является управляющим,**`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::iscntrl("A"));
var_dump(IntlChar::iscntrl(" "));
var_dump(IntlChar::iscntrl("\n"));
var_dump(IntlChar::iscntrl("\u{200e}"));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(false)
bool(true)
bool(true)
```

### Дивіться також

-   [IntlChar::isprint()](intlchar.isprint.md) \- Перевіряє, чи символ відображається
-   **`IntlChar::PROPERTY_DEFAULT_IGNORABLE_CODE_POINT`**
-   [ctype\_cntrl()](function.ctype-cntrl.md) \- Перевіряє керуючі символи
