---
navigation:
  - intlchar.fordigit.md: '« IntlChar::forDigit'
  - intlchar.getblockcode.md: 'IntlChar::getBlockCode »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::getBidiPairedBracket'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::getBidiPairedBracket

(PHP 7, PHP 8)

IntlChar::getBidiPairedBracket — Отримати парну дужку для символу

### Опис

```methodsynopsis
public static IntlChar::getBidiPairedBracket(int|string $codepoint): int|string|null
```

Отримує парну дужку для символу.

Для`Bidi_Paired_Bracket_Type!=None`, це аналогічно [IntlChar::charMirror()](intlchar.charmirror.md). Якщо такого немає, повертається вихідний `codepoint`

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

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

Результат виконання наведеного прикладу:

```
int(93)
string(1) "]"
```

### Дивіться також

-   [IntlChar::charMirror()](intlchar.charmirror.md) - Отримати "дзеркальний" символ за кодом
-   **`IntlChar::PROPERTY_BIDI_PAIRED_BRACKET`**
-   **`IntlChar::PROPERTY_BIDI_PAIRED_BRACKET_TYPE`**
