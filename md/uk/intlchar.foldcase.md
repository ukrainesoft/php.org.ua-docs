---
navigation:
  - intlchar.enumchartypes.md: '« IntlChar::enumCharTypes'
  - intlchar.fordigit.md: 'IntlChar::forDigit »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::foldCase'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::foldCase

(PHP 7, PHP 8)

IntlChar::foldCase — Перетворює регістр заданого символу.

### Опис

```methodsynopsis
public static IntlChar::foldCase(int|string $codepoint, int $options = IntlChar::FOLD_CASE_DEFAULT): int|string|null
```

Повертає код символу в регістрі відмінному від регістра переданого символу. Якщо символ не має уявлення в іншому регістрі, то буде повернутий переданий символ.

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

`options`

**`IntlChar::FOLD_CASE_DEFAULT`**(по умолчанию) или\*\*`IntlChar::FOLD_CASE_EXCLUDE_SPECIAL_I`\*\*

### Значення, що повертаються

Повертає *Simple\_Case\_Folding* для символу, якщо вона є. В іншому випадку - сам символ у разі успішного виконання або \*\*`null`\*\*в случае возникновения ошибки.
