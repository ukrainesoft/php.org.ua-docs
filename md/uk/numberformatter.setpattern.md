---
navigation:
  - numberformatter.setattribute.html: '« NumberFormatter::setAttribute'
  - numberformatter.setsymbol.html: 'NumberFormatter::setSymbol »'
  - index.html: PHP Manual
  - class.numberformatter.html: NumberFormatter
title: 'NumberFormatter::setPattern'
---
# NumberFormatter::setPattern

# numfmtsetpattern

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::setPattern -- numfmtsetpattern — Встановлює шаблон засобу форматування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::setPattern(string $pattern): bool
```

Процедурний стиль

```methodsynopsis
numfmt_set_pattern(NumberFormatter $formatter, string $pattern): bool
```

Встановлює шаблон, який використовується засобом форматування. Не може використовуватися у форматуванні на основі правил.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

`pattern`

Шаблон у синтаксисі, описаному в [» документации ICU DecimalFormat](http://www.icu-project.org/apiref/icu4c/classDecimalFormat.html#details)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **numfmtsetpattern()****

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Шаблон: ".numfmt_get_pattern($fmt)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
numfmt_set_pattern($fmt, "#0.# kg");
echo "Шаблон: ".numfmt_get_pattern($fmt)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Шаблон: ".$fmt->getPattern()."\n";
echo $fmt->format(1234567.891234567890000)."\n";
$fmt->setPattern("#0.# kg");
echo "Шаблон: ".$fmt->getPattern()."\n";
echo $fmt->format(1234567.891234567890000)."\n";
?>
```

Результат виконання цього прикладу:

```
Шаблон: #,##0.###
1.234.567,891
Шаблон: #0.# kg
1234567,9 kg
```

### Дивіться також

-   [numfmtgeterrorcode()](numberformatter.geterrorcode.md) - Отримує останній код помилки засобу форматування
-   [numfmtcreate()](numberformatter.create.md) - Створює засіб форматування чисел
-   [numfmtgetpattern()](numberformatter.getpattern.md) - Отримує шаблон засобу форматування
