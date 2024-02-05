---
navigation:
  - intlchar.getintpropertyvalue.md: '« IntlChar::getIntPropertyValue'
  - intlchar.getpropertyenum.md: 'IntlChar::getPropertyEnum »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::getNumericValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::getNumericValue

(PHP 7, PHP 8)

IntlChar::getNumericValue — Отримати числову виставу для символу Unicode

### Опис

```methodsynopsis
public static IntlChar::getNumericValue(int|string $codepoint): ?float
```

Отримує числове уявлення символу Unicode, як у базі символів Unicode.

Если для символа отсутствует численное представление - будет возвращено\*\*`IntlChar::NO_NUMERIC_VALUE`\*\*

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Численное значение`codepoint`, или\*\*`IntlChar::NO_NUMERIC_VALUE`\*\* якщо відсутня чи не задано. Ця константа з'явилася в PHP 7.0.6, до цієї версії у такому разі поверталося (float)`-123456789`. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::getNumericValue("4"));
var_dump(IntlChar::getNumericValue("x"));
var_dump(IntlChar::getNumericValue("\u{216C}"));
?>
```

Результат виконання наведеного прикладу:

```
float(4)
float(-123456789)
float(50)
```
