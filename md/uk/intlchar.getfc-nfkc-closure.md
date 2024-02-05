---
navigation:
  - intlchar.getcombiningclass.md: '« IntlChar::getCombiningClass'
  - intlchar.getintpropertymaxvalue.md: 'IntlChar::getIntPropertyMaxValue »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::getFC\_NFKC\_Closure'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::getFC\_NFKC\_Closure

(PHP 7, PHP 8)

IntlChar::getFC\_NFKC\_Closure — Отримати властивість FC\_NFKC\_Closure для символу

### Опис

```methodsynopsis
public static IntlChar::getFC_NFKC_Closure(int|string $codepoint): string|false|null
```

Отримує властивість FC\_NFKC\_Closure для символу.

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає властивість FC\_NFKC\_Closure для`codepoint` у вигляді рядка або порожній рядок, якщо його немає. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::getFC_NFKC_Closure("\u{2121}"));
var_dump(IntlChar::getFC_NFKC_Closure("\u{1D2D}"));
?>
```

Результат виконання наведеного прикладу:

```
string(3) "tel"
string(2) "æ"
```
