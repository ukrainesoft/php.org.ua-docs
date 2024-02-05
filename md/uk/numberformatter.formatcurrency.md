---
navigation:
  - numberformatter.create.md: '« NumberFormatter::create'
  - numberformatter.format.md: 'NumberFormatter::format »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::formatCurrency'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# NumberFormatter::formatCurrency

# numfmt\_format\_currency

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::formatCurrency -- numfmt\_format\_currency - Форматує значення валюти

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

Об'єкт [NumberFormatter](class.numberformatter.md)

`amount`

Числове значення валюти.

`currency`

Трилітерний код валюти ISO 4217, що позначає валюту, що використовується.

### Значення, що повертаються

Рядок, що становить форматоване значення валюти або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** numfmt\_format\_currency()\*\*\*\*

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::CURRENCY );
echo numfmt_format_currency($fmt, 1234567.891234567890000, "EUR")."\n";
echo numfmt_format_currency($fmt, 1234567.891234567890000, "RUR")."\n";
$fmt = numfmt_create( 'ru_RU', NumberFormatter::CURRENCY );
echo numfmt_format_currency($fmt, 1234567.891234567890000, "EUR")."\n";
echo numfmt_format_currency($fmt, 1234567.891234567890000, "RUR")."\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::CURRENCY );
echo $fmt->formatCurrency(1234567.891234567890000, "EUR")."\n";
echo $fmt->formatCurrency(1234567.891234567890000, "RUR")."\n";
$fmt = new NumberFormatter( 'ru_RU', NumberFormatter::CURRENCY );
echo $fmt->formatCurrency(1234567.891234567890000, "EUR")."\n";
echo $fmt->formatCurrency(1234567.891234567890000, "RUR")."\n";
?>
```

Результат виконання наведеного прикладу:

```
1.234.567,89 €
1.234.567,89 RUR
1 234 567,89€
1 234 567,89р.
```

### Примітки

> **Зауваження** :
> 
> Формати, досягнуті цим способом форматування, не можуть повністю використовувати можливості базової бібліотеки ICU, наприклад форматувати валюту з вузьким символом валюти.
> 
> Для полной поддержки, используйте функцию[msgfmt\_format\_message()](messageformatter.formatmessage.md)

### Дивіться також

-   [numfmt\_get\_error\_code()](numberformatter.geterrorcode.md) \- Отримує останній код помилки засобу форматування
-   [numfmt\_format()](numberformatter.format.md) \- Форматує число
-   [numfmt\_parse\_currency()](numberformatter.parsecurrency.md) \- Розбирає номер валюти
-   [msgfmt\_format\_message()](messageformatter.formatmessage.md) \- Швидко форматує повідомлення
