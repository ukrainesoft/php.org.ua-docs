---
navigation:
  - intlchar.charage.md: '« IntlChar::charAge'
  - intlchar.chardirection.md: 'IntlChar::charDirection »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::charDigitValue'
---
# IntlChar::charDigitValue

(PHP 7, PHP 8)

IntlChar::charDigitValue — Отримати десяткову цифру із символу десяткової цифри

### Опис

```methodsynopsis
public static IntlChar::charDigitValue(int|string $codepoint): ?int
```

Отримує Отримати десяткову цифру із символу десяткової цифри.

Такі символи входять у глобальну категорію "Nd" (десяткові цифри) та NumericType в Decimal.

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Цифра, що відповідає символу `codepoint`, або `-1` якщо символ не є десятковою цифрою. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::charDigitValue("1"));
var_dump(IntlChar::charDigitValue("\u{0662}"));
var_dump(IntlChar::charDigitValue("\u{0E53}"));
?>
```

Результат виконання цього прикладу:

```
int(1)
int(2)
int(3)
```

### Дивіться також

-   [IntlChar::getNumericValue()](intlchar.getnumericvalue.md) - Отримати числову виставу для символу Unicode
