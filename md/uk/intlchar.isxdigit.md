---
navigation:
  - intlchar.iswhitespace.md: '« IntlChar::isWhitespace'
  - intlchar.ord.md: 'IntlChar::ord »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isxdigit'
---
# IntlChar::isxdigit

(PHP 7, PHP 8)

IntlChar::isxdigit — Перевірити, чи є символ шістнадцятковою цифрою

### Опис

```methodsynopsis
public static IntlChar::isxdigit(int|string $codepoint): ?bool
```

Перевіряє, чи є символ шістнадцятковою цифрою.

**`true`** для символів з категорії "Nd" (десяткові цифри) і латинських літер a-f і A-F в уявленнях ASCII і Fullwidth ASCII (0041..0046, 0061..0066, FF21..FF26, FF41..FF46.)

Еквівалентно `IntlChar::digit($codepoint, 16) >= 0`

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є шістнадцятковою цифрою, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isxdigit("A"));
var_dump(IntlChar::isxdigit("1"));
var_dump(IntlChar::isxdigit("\u{2603}"));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(true)
bool(false)
```

### Примітки

> **Зауваження**
> 
> Для того щоб звузити визначення шістнадцяткових цифр приймаються тільки символи ASCII:
> 
> ```php
> <?php
> $isASCIIHexadecimal = IntlChar::ord($codepoint) <= 0x7F && IntlChar::isxdigit($codepoint);
> ?>
> ```

### Дивіться також

-   [IntlChar::isdigit()](intlchar.isdigit.md) - Перевірити, чи є символ цифрою
