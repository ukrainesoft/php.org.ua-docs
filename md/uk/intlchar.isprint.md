---
navigation:
  - intlchar.ismirrored.md: '« IntlChar::isMirrored'
  - intlchar.ispunct.md: 'IntlChar::ispunct »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isprint'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isprint

(PHP 7, PHP 8)

IntlChar::isprint — Перевіряє, чи символ відображається.

### Опис

```methodsynopsis
public static IntlChar::isprint(int|string $codepoint): ?bool
```

Перевіряє, чи символ відображається.

**`true`** для категорій, відмінних від "C" (керуючі символи).

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є символом, що відображається, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isprint("A"));
var_dump(IntlChar::isprint(" "));
var_dump(IntlChar::isprint("\n"));
var_dump(IntlChar::isprint("\u{200e}"));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
bool(false)
bool(false)
```

### Дивіться також

-   [IntlChar::iscntrl()](intlchar.iscntrl.md) \- Перевірити, чи є символ керуючим
-   **`IntlChar::PROPERTY_DEFAULT_IGNORABLE_CODE_POINT`**
-   [ctype\_print()](function.ctype-print.md) \- Перевіряє друковані символи
