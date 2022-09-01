---
navigation:
  - intlchar.ord.md: '« IntlChar::ord'
  - intlchar.totitle.md: 'IntlChar::totitle »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::tolower'
---
# IntlChar::tolower

(PHP 7, PHP 8)

IntlChar::tolower — Перетворення символу Unicode на нижній регістр

### Опис

```methodsynopsis
public static IntlChar::tolower(int|string $codepoint): int|string|null
```

Перетворює символ на його еквівалент у нижньому регістрі. Якщо немає, то повертається вихідний символ.

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає SimpleLowercaseMapping для символу, якщо існує. Якщо ні, повертає вихідний символ. У разі виникнення помилки повертає **`null`**

Тип, що повертається повинен бути int, якщо тільки символ не був переданий як рядок UTF-8 (string), у цьому випадку повернеться рядок (string). У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::tolower("A"));
var_dump(IntlChar::tolower("a"));
var_dump(IntlChar::tolower("Φ"));
var_dump(IntlChar::tolower("φ"));
var_dump(IntlChar::tolower("1"));
var_dump(IntlChar::tolower(ord("A")));
var_dump(IntlChar::tolower(ord("a")));
?>
```

Результат виконання цього прикладу:

```
string(1) "a"
string(1) "a"
string(2) "φ"
string(2) "φ"
string(1) "1"
int(97)
int(97)
```

### Дивіться також

-   [IntlChar::totitle()](intlchar.totitle.md) - Перетворює символ Unicode у titlecase
-   [IntlChar::toupper()](intlchar.toupper.md) - Перетворення символу Unicode у верхній регістр
-   [мбstrtolower()](function.mb-strtolower.html) - Приведення рядка до нижнього регістру
