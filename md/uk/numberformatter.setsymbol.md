Встановлює значення символу

-   [« NumberFormatter::setPattern](numberformatter.setpattern.md)
    
-   [NumberFormatter::setTextAttribute »](numberformatter.settextattribute.md)
    
-   [PHP Manual](index.md)
    
-   [NumberFormatter](class.numberformatter.md)
    
-   Встановлює значення символу
    

# NumberFormatter::setSymbol

# numfmtsetsymbol

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::setSymbol -- numfmtsetsymbol — Встановлює значення символу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::setSymbol(int $symbol, string $value): bool
```

Процедурний стиль

```methodsynopsis
numfmt_set_symbol(NumberFormatter $formatter, int $symbol, string $value): bool
```

Встановлює символ, пов'язаний із засобом форматування. Засіб форматування використовує символи для представлення спеціальних символів, які залежать від мови, у числах, наприклад, знак відсотка. Цей API не підтримується для форматування на основі правил.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

`symbol`

Специфікатор символу, одна з констант [символа форматирования](class.numberformatter.html#intl.numberformatter-constants.unumberformatsymbol)

`value`

Текст для символу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **numfmtsetsymbol()****

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Разделитель: ".numfmt_get_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
numfmt_set_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL, "*");
echo "Разделитель: ".numfmt_get_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Разделитель: ".$fmt->getSymbol(NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
$fmt->setSymbol(NumberFormatter::GROUPING_SEPARATOR_SYMBOL, "*");
echo "Разделитель: ".$fmt->getSymbol(NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
?>
```

Результат виконання цього прикладу:

```
Разделитель: .
1.234.567,891
Разделитель: *
1*234*567,891
```

### Дивіться також

-   [numfmtgeterrorcode()](numberformatter.geterrorcode.md) - Отримує останній код помилки засобу форматування
-   [numfmtgetsymbol()](numberformatter.getsymbol.md) - Отримує значення символу