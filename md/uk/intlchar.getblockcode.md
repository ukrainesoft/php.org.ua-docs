---
navigation:
  - intlchar.getbidipairedbracket.md: '« IntlChar::getBidiPairedBracket'
  - intlchar.getcombiningclass.md: 'IntlChar::getCombiningClass »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::getBlockCode'
---
# IntlChar::getBlockCode

(PHP 7, PHP 8)

IntlChar::getBlockCode — Отримати блок розміщення символу Unicode

### Опис

```methodsynopsis
public static IntlChar::getBlockCode(int|string $codepoint): ?int
```

Повертає блок розміщення символу Unicode.

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає блок розміщення `codepoint`. Одна з констант `IntlChar::BLOCK_CODE_*`. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::getBlockCode("A") === IntlChar::BLOCK_CODE_BASIC_LATIN);
var_dump(IntlChar::getBlockCode("Φ") === IntlChar::BLOCK_CODE_GREEK);
var_dump(IntlChar::getBlockCode("\u{2603}") === IntlChar::BLOCK_CODE_MISCELLANEOUS_SYMBOLS);
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(true)
bool(true)
```
