---
navigation:
  - intlchar.isidstart.md: '« IntlChar::isIDStart'
  - intlchar.isjavaidpart.md: 'IntlChar::isJavaIDPart »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isISOControl'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isISOControl

(PHP 7, PHP 8)

IntlChar::isISOControl — Перевірити, чи є символ керуючим відповідно до ISO

### Опис

```methodsynopsis
public static IntlChar::isISOControl(int|string $codepoint): ?bool
```

Перевіряє, чи є символ керуючим відповідно до ISO.

**`true`** для U+0000..U+001f та U+007f..U+009f (категорія "Cc").

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint`является управляющим символом ISO,**`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isISOControl(" "));
var_dump(IntlChar::isISOControl("\n"));
var_dump(IntlChar::isISOControl("\u{200e}"));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
bool(false)
```

### Дивіться також

-   [IntlChar::iscntrl()](intlchar.iscntrl.md) \- Перевірити, чи є символ керуючим
