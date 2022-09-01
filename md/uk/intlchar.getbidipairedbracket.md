---
navigation:
  - intlchar.fordigit.html: '« IntlChar::forDigit'
  - intlchar.getblockcode.html: 'IntlChar::getBlockCode »'
  - index.html: PHP Manual
  - class.intlchar.html: IntlChar
title: 'IntlChar::getBidiPairedBracket'
---
# IntlChar::getBidiPairedBracket

(PHP 7, PHP 8)

IntlChar::getBidiPairedBracket — Отримати парну дужку для символу

### Опис

```methodsynopsis
public static IntlChar::getBidiPairedBracket(int|string $codepoint): int|string|null
```

Отримує парну дужку для символу.

Для `Bidi_Paired_Bracket_Type!=None`, це аналогічно [IntlChar::charMirror()](intlchar.charmirror.html). Якщо такого немає, повертається вихідний `codepoint`

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає парну дужку для символу, або `codepoint` якщо такої немає. У разі виникнення помилки повертає **`null`**

Тип, що повертається повинен бути int, якщо тільки символ не був переданий як рядок UTF-8 (string), у цьому випадку повернеться рядок (string). У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::getBidiPairedBracket(91));
var_dump(IntlChar::getBidiPairedBracket('['));
?>
```

Результат виконання цього прикладу:

```
int(93)
string(1) "]"
```

### Дивіться також

-   [IntlChar::charMirror()](intlchar.charmirror.html) - Отримати "дзеркальний" символ за кодом
-   **`IntlChar::PROPERTY_BIDI_PAIRED_BRACKET`**
-   **`IntlChar::PROPERTY_BIDI_PAIRED_BRACKET_TYPE`**
