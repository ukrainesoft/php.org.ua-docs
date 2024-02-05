---
navigation:
  - intlchar.isgraph.md: '« IntlChar::isgraph'
  - intlchar.isidpart.md: 'IntlChar::isIDPart »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isIDIgnorable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isIDIgnorable

(PHP 7, PHP 8)

IntlChar::isIDIgnorable — Перевірити, чи символ ігнорується

### Опис

```methodsynopsis
public static IntlChar::isIDIgnorable(int|string $codepoint): ?bool
```

Перевіряє, чи символ ігнорується в ідентифікаторах.

**`true`** для символів з категорії "Cf" (управління форматом) та не пробельних керуючих символів ISO (U+0000..U+0008, U+000E..U+001B, U+007F..U+009F).

> **Зауваження** :
> 
> Зверніть увагу на те, що Unicode просто рекомендує ігнорувати Cf (управління форматом).

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` ігнорується в ідентифікаторах, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isIDIgnorable("A"));
var_dump(IntlChar::isIDIgnorable(" "));
var_dump(IntlChar::isIDIgnorable("\u{007F}"));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(false)
bool(true)
```

### Дивіться також

-   [IntlChar::isIDStart()](intlchar.isidstart.md) \- Перевірити, чи можна використовувати символ на початку ідентифікатора
-   [IntlChar::isIDPart()](intlchar.isidpart.md) \- Перевірити, чи можна використовувати символ в ідентифікаторі
-   **`IntlChar::PROPERTY_DEFAULT_IGNORABLE_CODE_POINT`**
