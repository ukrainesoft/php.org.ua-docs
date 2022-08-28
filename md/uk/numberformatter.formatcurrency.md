Форматує значення валюти

-   [« NumberFormatter::create](numberformatter.create.html)
    
-   [NumberFormatter::format »](numberformatter.format.html)
    
-   [PHP Manual](index.html)
    
-   [NumberFormatter](class.numberformatter.html)
    
-   Форматує значення валюти
    

# NumberFormatter::formatCurrency

# numfmtformatcurrency

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::formatCurrency -- numfmtformatcurrency - Форматує значення валюти

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::formatCurrency(float $amount, string $currency): string|false
```

Процедурний стиль

```methodsynopsis
numfmt_format_currency(NumberFormatter $formatter, float $amount, string $currency): string|false
```

Форматує значення валюти відповідно до правил форматування.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.html)

`amount`

Числове значення валюти.

`currency`

Трилітерний код валюти ISO 4217, що позначає валюту, що використовується.

### Значення, що повертаються

Рядок, що становить форматоване значення валюти або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **numfmtformatcurrency()****

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::CURRENCY );
echo numfmt_format_currency($fmt, 1234567.891234567890000, "EUR")."\n";
echo numfmt_format_currency($fmt, 1234567.891234567890000, "RUR")."\n";
$fmt = numfmt_create( 'ru_RU', NumberFormatter::CURRENCY );
echo numfmt_format_currency($fmt, 1234567.891234567890000, "EUR")."\n";
echo numfmt_format_currency($fmt, 1234567.891234567890000, "RUR")."\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::CURRENCY );
echo $fmt->formatCurrency(1234567.891234567890000, "EUR")."\n";
echo $fmt->formatCurrency(1234567.891234567890000, "RUR")."\n";
$fmt = new NumberFormatter( 'ru_RU', NumberFormatter::CURRENCY );
echo $fmt->formatCurrency(1234567.891234567890000, "EUR")."\n";
echo $fmt->formatCurrency(1234567.891234567890000, "RUR")."\n";
?>
```

Результат виконання цього прикладу:

```
1.234.567,89 €
1.234.567,89 RUR
1 234 567,89€
1 234 567,89р.
```

### Дивіться також

-   [numfmt\_get\_error\_code()](numberformatter.geterrorcode.html) - Отримує останній код помилки засобу форматування
-   [numfmt\_format()](numberformatter.format.html) - Форматує число
-   [numfmt\_parse\_currency()](numberformatter.parsecurrency.html) - Розбирає номер валюти