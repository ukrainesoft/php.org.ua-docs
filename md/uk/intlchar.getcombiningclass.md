---
navigation:
  - intlchar.getblockcode.md: '« IntlChar::getBlockCode'
  - intlchar.getfc-nfkc-closure.md: 'IntlChar::getFC\_NFKC\_Closure »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::getCombiningClass'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::getCombiningClass

(PHP 7, PHP 8)

IntlChar::getCombiningClass — Отримати комбінуючий клас для символу

### Опис

```methodsynopsis
public static IntlChar::getCombiningClass(int|string $codepoint): ?int
```

Повертає комбінуючий клас для символу.

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає комбінуючий клас для символу. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::getCombiningClass("A"));
var_dump(IntlChar::getCombiningClass("\u{0334}"));
var_dump(IntlChar::getCombiningClass("\u{0358}"));
?>
```

Результат виконання наведеного прикладу:

```
int(0)
int(1)
int(232)
```
