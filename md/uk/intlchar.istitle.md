---
navigation:
  - intlchar.isspace.md: '« IntlChar::isspace'
  - intlchar.isualphabetic.md: 'IntlChar::isUAlphabetic »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::istitle'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::istitle

(PHP 7, PHP 8)

IntlChar::istitle — Перевірити, чи символ є титульним (Titlecase)

### Опис

```methodsynopsis
public static IntlChar::istitle(int|string $codepoint): ?bool
```

Перевірити, чи символ входить до категорії Titlecase. Дані символи є складовими з кількох літер, перша з яких велика. Наприклад \\u{01cb} (ǋ) или\\u{1faf} (ᾯ).

**`true`** для категорії "Lt" (titlecase).

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є титульним символом, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php

// Латинская заглавная буква Dz с гачеком U+01C4
var_dump(IntlChar::istitle("Ǆ"));

// Латинская заглавная буква D с маленькой буквой Z с гачеком U+01C5
var_dump(IntlChar::istitle("ǅ"));

// Латинская строчная буква Dz с гачеком U+01C6
var_dump(IntlChar::istitle("ǆ"));

// Греческая заглавная буква Alpha с подстрочной йотой U+1FBC
var_dump(IntlChar::istitle("ᾼ"));

// Греческая малая буква Alpha с подстрочной йотой U+1FB3
var_dump(IntlChar::istitle("ᾳ"));

// Греческая заглавная буква Alpha
var_dump(IntlChar::istitle("Α"));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
bool(false)
bool(true)
bool(false)
bool(false)
```

### Дивіться також

-   [IntlChar::isupper()](intlchar.isupper.md) - Перевірити, чи входить символ у категорію "Lu" (літера у верхньому регістрі)
-   [IntlChar::islower()](intlchar.islower.md) \- Перевірити, чи в нижньому регістрі символ
-   [IntlChar::totitle()](intlchar.totitle.md) \- Перетворює символ Unicode на титульний регістр (titlecase)
