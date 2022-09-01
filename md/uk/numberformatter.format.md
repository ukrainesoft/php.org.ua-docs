---
navigation:
  - numberformatter.formatcurrency.html: '« NumberFormatter::formatCurrency'
  - numberformatter.getattribute.html: 'NumberFormatter::getAttribute »'
  - index.html: PHP Manual
  - class.numberformatter.html: NumberFormatter
title: 'NumberFormatter::format'
---
# NumberFormatter::format

# numfmtformat

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::format -- numfmtformat — Форматує число

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::format(int|float $num, int $type = NumberFormatter::TYPE_DEFAULT): string|false
```

Процедурний стиль

```methodsynopsis
numfmt_format(NumberFormatter $formatter, int|float $num, int $type = NumberFormatter::TYPE_DEFAULT): string|false
```

Форматує числове значення відповідно до правил засобу форматування.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.html)

`num`

Значення форматування. Може бути цілим числом (int) або числом з плаваючою точкою (float), інші типи будуть перетворені на числове значення.

`type`

Використовуваний [тип форматирования](class.numberformatter.html#intl.numberformatter-constants.types)

### Значення, що повертаються

Повертає рядок, який містить форматоване значення або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **numfmtformat()****

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
$data = numfmt_format($fmt, 1234567.891234567890000);
if(intl_is_failure(numfmt_format($fmt))) {
    report_error("Formatter error");
}
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
$fmt->format(1234567.891234567890000);
if(intl_is_failure($fmt->getErrorCode())) {
    report_error("Formatter error");
}
?>
```

Результат виконання цього прикладу:

```
1.234.567,891
```

### Дивіться також

-   [numfmtgeterrorcode()](numberformatter.geterrorcode.html) - Отримує останній код помилки засобу форматування
-   [numfmtformatcurrency()](numberformatter.formatcurrency.html) - Форматує значення валюти
-   [numfmtparse()](numberformatter.parse.html) - Розбирає число
