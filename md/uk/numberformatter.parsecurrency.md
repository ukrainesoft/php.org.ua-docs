---
navigation:
  - numberformatter.gettextattribute.md: '« NumberFormatter::getTextAttribute'
  - numberformatter.parse.md: 'NumberFormatter::parse »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::parseCurrency'
---
# NumberFormatter::parseCurrency

# numfmtparsecurrency

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::parseCurrency - numfmtparsecurrency — Розбирає номер валюти

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::parseCurrency(string $string, string &$currency, int &$offset = null): float|false
```

Процедурний стиль

```methodsynopsis
numfmt_parse_currency(    NumberFormatter $formatter,    string $string,    string &$currency,    int &$offset = null): float|false
```

Розбирає рядок на число з плаваючою точкою та валюту за допомогою засобу форматування.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

`currency`

Параметр для отримання назви валюти (трилітерний код валюти ISO 4217).

`offset`

Зміщення у рядку, з якого починається синтаксичний аналіз. При поверненні це значення міститиме усунення, у якому закінчився синтаксичний аналіз.

### Значення, що повертаються

Розібране числове значення або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **numfmtparsecurrency()****

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::CURRENCY );
$num = "1.234.567,89\xc2\xa0$";
echo "У нас ".numfmt_parse_currency($fmt, $num, $curr)." в $curr\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::CURRENCY );
$num = "1.234.567,89\xc2\xa0$";
echo "У нас ".$fmt->parseCurrency($num, $curr)." в $curr\n";
?>
```

Результат виконання цього прикладу:

```
У нас 1234567.89 в USD
```

### Дивіться також

-   [numfmtgeterrorcode()](numberformatter.geterrorcode.md) - Отримує останній код помилки засобу форматування
-   [numfmtparse()](numberformatter.parse.md) - Розбирає число
-   [numfmtformatcurrency()](numberformatter.formatcurrency.md) - Форматує значення валюти
