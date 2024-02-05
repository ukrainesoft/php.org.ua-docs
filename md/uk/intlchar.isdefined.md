---
navigation:
  - intlchar.iscntrl.md: '« IntlChar::iscntrl'
  - intlchar.isdigit.md: 'IntlChar::isdigit »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isdefined'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isdefined

(PHP 7, PHP 8)

IntlChar::isdefined — Перевірити, чи є символ.

### Опис

```methodsynopsis
public static IntlChar::isdefined(int|string $codepoint): ?bool
```

Перевіряє, чи є символ. Зазвичай це означає, що код Unicode призначений конкретний символ.

**`true`** для категорій, відмінних від "Cn" (інші, не призначені).

> **Зауваження** :
> 
> Note that non-character code points (e.g., U+FDD0) are not "defined" (they are Cn), but surrogate code points are "defined" (Cs).

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є певним, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isdefined("A"));
var_dump(IntlChar::isdefined(" "));
var_dump(IntlChar::isdefined("\u{FDD0}"));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
bool(false)
```

### Дивіться також

-   [IntlChar::isdigit()](intlchar.isdigit.md) \- Перевірити, чи є символ цифрою
-   [IntlChar::isalpha()](intlchar.isalpha.md) \- Перевірити, чи є символ літерою
-   [IntlChar::isalnum()](intlchar.isalnum.md) \- Перевірити, чи є символ буквою чи цифрою
-   [IntlChar::isupper()](intlchar.isupper.md) - Перевірити, чи входить символ у категорію "Lu" (літера у верхньому регістрі)
-   [IntlChar::islower()](intlchar.islower.md) \- Перевірити, чи в нижньому регістрі символ
-   [IntlChar::istitle()](intlchar.istitle.md) \- Перевірити, чи символ є титульним (Titlecase)
