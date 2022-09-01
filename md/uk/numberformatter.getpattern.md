---
navigation:
  - numberformatter.getlocale.md: '« NumberFormatter::getLocale'
  - numberformatter.getsymbol.md: 'NumberFormatter::getSymbol »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::getPattern'
---
# NumberFormatter::getPattern

# numfmtgetpattern

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::getPattern -- numfmtgetpattern — Отримує шаблон засобу форматування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::getPattern(): string|false
```

Процедурний стиль

```methodsynopsis
numfmt_get_pattern(NumberFormatter $formatter): string|false
```

Витягує шаблон, який використовується засобом форматування.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

### Значення, що повертаються

Рядок (string) шаблону, що використовується засобом форматування або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **numfmtgetpattern()****

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
-   [numfmtsetpattern()](numberformatter.setpattern.md) - Встановлює шаблон засобу форматування
-   [numfmtcreate()](numberformatter.create.md) - Створює засіб форматування чисел
