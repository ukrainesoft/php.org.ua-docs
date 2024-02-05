---
navigation:
  - intlchar.tolower.md: '« IntlChar::tolower'
  - intlchar.toupper.md: 'IntlChar::toupper »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::totitle'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::totitle

(PHP 7, PHP 8)

IntlChar::totitle — Перетворює символ Unicode на титульний регістр (titlecase)

### Опис

```methodsynopsis
public static IntlChar::totitle(int|string $codepoint): int|string|null
```

Повертає еквівалент символу в титульному (titlecase) регістрі. Якщо немає, то повертається вихідний символ.

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає Просте\_Зіставлення\_в\_Титульному\_Реєстр (Simple\_Titlecase\_Mapping) для символу, якщо існує. Якщо ні, повертає вихідний символ. У разі виникнення помилки повертає **`null`**

Тип, що повертається повинен бути int, якщо тільки символ не був переданий як рядок UTF-8 (string), у цьому випадку повернеться рядок (string). У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php

var_dump(IntlChar::totitle("Ǆ"));
var_dump(IntlChar::totitle("ǆ"));
var_dump(IntlChar::totitle("Φ"));
var_dump(IntlChar::totitle("φ"));
var_dump(IntlChar::totitle("1"));
var_dump(IntlChar::totitle("ᾳ");
var_dump(IntlChar::totitle(ord("A")));
?>
```

Результат виконання наведеного прикладу:

```
string(1) "ǅ"
string(1) "ǅ"
string(2) "Φ"
string(2) "φ"
string(1) "1"
string(1) "ᾼ"
int(65)
```

### Дивіться також

-   [IntlChar::tolower()](intlchar.tolower.md) \- Перетворює символ Unicode на нижній регістр
-   [IntlChar::toupper()](intlchar.toupper.md) \- Перетворює символ Unicode у верхній регістр
-   [IntlChar::istitle()](intlchar.istitle.md) \- Перевірити, чи символ є титульним (Titlecase)
-   [mb\_convert\_case()](function.mb-convert-case.md) \- Змінює регістр символів у рядку
