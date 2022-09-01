---
navigation:
  - intlchar.isidpart.md: '« IntlChar::isIDPart'
  - intlchar.isisocontrol.md: 'IntlChar::isISOControl »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isIDStart'
---
# IntlChar::isIDStart

(PHP 7, PHP 8)

IntlChar::isIDStart — Перевірити, чи можна використовувати символ на початку ідентифікатора

### Опис

```methodsynopsis
public static IntlChar::isIDStart(int|string $codepoint): ?bool
```

Перевіряє, чи можна використовувати символ на початку ідентифікатора відповідно до стандарту Unicode (The Unicode Standard, версія 3.0, розділ 5.16 - Ідентифікатори).

**`true`** для категорій "L" (літери) та "Nl" (символи цифр).

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає **`true`** якщо `codepoint` можна використовувати на початку ідентифікатора, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isIDStart("A"));
var_dump(IntlChar::isIDStart("$"));
var_dump(IntlChar::isIDStart("\n"));
var_dump(IntlChar::isIDStart("\u{2603}"));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
bool(false)
bool(false)
```

### Дивіться також

-   [IntlChar::isalpha()](intlchar.isalpha.md) - Перевірити, чи є символ літерою
-   [IntlChar::isIDPart()](intlchar.isidpart.md) - Перевірити, чи можна використовувати символ в ідентифікаторі
-   **`IntlChar::PROPERTY_ID_START`**
