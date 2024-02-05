---
navigation:
  - intlchar.totitle.md: '« IntlChar::totitle'
  - class.intlexception.md: IntlException »
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::toupper'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::toupper

(PHP 7, PHP 8)

IntlChar::toupper — Перетворює символ Unicode у верхній регістр

### Опис

```methodsynopsis
public static IntlChar::toupper(int|string $codepoint): int|string|null
```

Перетворює символ на його еквівалент у верхньому регістрі. Якщо цього немає, то повертається вихідний символ.

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає Simple\_Uppercase\_Mapping символ, якщо він є; інакше повертається вихідний символ.

Тип, що повертається повинен бути int, якщо тільки символ не був переданий як рядок UTF-8 (string), у цьому випадку повернеться рядок (string). У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::toupper("A"));
var_dump(IntlChar::toupper("a"));
var_dump(IntlChar::toupper("Φ"));
var_dump(IntlChar::toupper("φ"));
var_dump(IntlChar::toupper("1"));
var_dump(IntlChar::toupper(ord("A")));
var_dump(IntlChar::toupper(ord("a")));
?>
```

Результат виконання наведеного прикладу:

```
string(1) "A"
string(1) "A"
string(2) "Φ"
string(2) "Φ"
string(1) "1"
int(65)
int(65)
```

### Дивіться також

-   [IntlChar::tolower()](intlchar.tolower.md) \- Перетворює символ Unicode на нижній регістр
-   [IntlChar::totitle()](intlchar.totitle.md) \- Перетворює символ Unicode на титульний регістр (titlecase)
-   [mb\_strtoupper()](function.mb-strtoupper.md) \- Приведе рядок до верхнього регістру
