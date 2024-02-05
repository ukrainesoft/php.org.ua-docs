---
navigation:
  - numberformatter.setpattern.md: '« NumberFormatter::setPattern'
  - numberformatter.settextattribute.md: 'NumberFormatter::setTextAttribute »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::setSymbol'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# NumberFormatter::setSymbol

# numfmt\_set\_symbol

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::setSymbol -- numfmt\_set\_symbol — Встановлює значення символу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::setSymbol(int $symbol, string $value): bool
```

Процедурний стиль

```methodsynopsis
numfmt_set_symbol(NumberFormatter $formatter, int $symbol, string $value): bool
```

Встановлює символ, пов'язаний із засобом форматування. Засіб форматування використовує символи для представлення спеціальних символів, що залежать від мови, у числах, наприклад, знак відсотка. Цей API не підтримується для форматування на основі правил.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

`symbol`

Спецификатор символа, одна из констант[символу форматування](class.numberformatter.md#intl.numberformatter-constants.unumberformatsymbol)

`value`

Текст для символу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** numfmt\_set\_symbol()\*\*\*\*

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Разделитель: ".numfmt_get_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
numfmt_set_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL, "*");
echo "Разделитель: ".numfmt_get_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
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
-   [numfmt\_get\_symbol()](numberformatter.getsymbol.md) \- Отримує значення символу
