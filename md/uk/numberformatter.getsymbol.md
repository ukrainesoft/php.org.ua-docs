---
navigation:
  - numberformatter.getpattern.md: '« NumberFormatter::getPattern'
  - numberformatter.gettextattribute.md: 'NumberFormatter::getTextAttribute »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::getSymbol'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# NumberFormatter::getSymbol

# numfmt\_get\_symbol

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::getSymbol -- numfmt\_get\_symbol — Отримує значення символу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::getSymbol(int $symbol): string|false
```

Процедурний стиль

```methodsynopsis
numfmt_get_symbol(NumberFormatter $formatter, int $symbol): string|false
```

Отримує символ, пов'язаний із засобом форматування. Засіб форматування використовує символи для представлення спеціальних символів, що залежать від мови, у числах, наприклад, знак відсотка. Цей API не підтримується для форматування на основі правил.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

`symbol`

Спецификатор символа, одна из констант[символів форматування](class.numberformatter.md#intl.numberformatter-constants.unumberformatsymbol)

### Значення, що повертаються

Строка символа или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**numfmt\_get\_symbol()\*\*\*\*

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Sep: ".numfmt_get_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
numfmt_set_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL, "*");
echo "Sep: ".numfmt_get_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Разделитель: ".$fmt->getSymbol(NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
$fmt->setSymbol(NumberFormatter::GROUPING_SEPARATOR_SYMBOL, "*");
echo "Разделитель: ".$fmt->getSymbol(NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
?>
```

Результат виконання наведеного прикладу:

```
Разделитель: .
1.234.567,891
Разделитель: *
1*234*567,891
```

### Дивіться також

-   [numfmt\_get\_error\_code()](numberformatter.geterrorcode.md) \- Отримує останній код помилки засобу форматування
-   [numfmt\_set\_symbol()](numberformatter.setsymbol.md) \- Встановлює значення символу
