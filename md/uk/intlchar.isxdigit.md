---
navigation:
  - intlchar.iswhitespace.md: '« IntlChar::isWhitespace'
  - intlchar.ord.md: 'IntlChar::ord »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isxdigit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isxdigit

(PHP 7, PHP 8)

IntlChar::isxdigit — Перевіряє, чи кодова точка відноситься до шістнадцяткової цифри

### Опис

```methodsynopsis
public static IntlChar::isxdigit(int|string $codepoint): ?bool
```

Перевіряє, чи кодова точка відноситься до шістнадцяткової цифри.

**`true`** для символів загальної категорії «Nd» (десяткові числа), а також латинських літер a-f та A-F як у уявленнях ASCII, так і у поданні ASCII повної ширини. (Тобто для букв з кодовими точками 0041..0046, 0061..0066, FF21..FF26, FF41..FF46.)

Еквівалентно `IntlChar::digit($codepoint, 16) >= 0`

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо кодова точка `codepoint` — це шістнадцятковий символ, або **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php

var_dump(IntlChar::isxdigit("A"));
var_dump(IntlChar::isxdigit("1"));
var_dump(IntlChar::isxdigit("\u{2603}"));

?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
bool(false)
```

### Примітки

> **Зауваження** :
> 
> Щоб звузити визначення шістнадцяткових цифр, приймаються лише ASCII-символи:
> 
> ```php
> <?php
> 
> $isASCIIHexadecimal = IntlChar::ord($codepoint) <= 0x7F && IntlChar::isxdigit($codepoint);
> 
> ?>
> ```

### Дивіться також

-   [IntlChar::isdigit()](intlchar.isdigit.md) \- Перевірити, чи є символ цифрою
-   [ctype\_xdigit()](function.ctype-xdigit.md) \- Перевіряє шістнадцяткові цифри
