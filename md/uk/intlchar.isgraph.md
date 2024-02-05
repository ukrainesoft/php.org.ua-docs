---
navigation:
  - intlchar.isdigit.md: '« IntlChar::isdigit'
  - intlchar.isidignorable.md: 'IntlChar::isIDIgnorable »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isgraph'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isgraph

(PHP 7, PHP 8)

IntlChar::isgraph — Перевірити, чи є символом графічним символом

### Опис

```methodsynopsis
public static IntlChar::isgraph(int|string $codepoint): ?bool
```

Перевіряє, чи є символ "графічним" символом (друковані символи, крім пробельних).

**`true`** для всіх символів за винятком вхідних у категорії "Cc" (керуючі символи), "Cf" (управління форматом), "Cs" (сурогати), "Cn" (не задані) та "Z" (розділювачі).

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` є "графічним" символом, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isgraph("A"));
var_dump(IntlChar::isgraph("1"));
var_dump(IntlChar::isgraph("\u{2603}"));
var_dump(IntlChar::isgraph("\n"));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
bool(true)
bool(false)
```

### Дивіться також

-   [ctype\_graph()](function.ctype-graph.md) \- Перевіряє будь-які друковані символи крім пробілу
