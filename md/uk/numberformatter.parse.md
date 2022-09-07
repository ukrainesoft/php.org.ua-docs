---
navigation:
  - numberformatter.parsecurrency.md: '« NumberFormatter::parseCurrency'
  - numberformatter.setattribute.md: 'NumberFormatter::setAttribute »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::parse'
---
# NumberFormatter::parse

# numfmtparse

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::parse -- numfmtparse — Розбирає число

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::parse(string $string, int $type = NumberFormatter::TYPE_DOUBLE, int &$offset = null): int|float|false
```

Процедурний стиль

```methodsynopsis
numfmt_parse(    NumberFormatter $formatter,    string $string,    int $type = NumberFormatter::TYPE_DOUBLE,    int &$offset = null): int|float|false
```

Перетворює рядок на число, використовуючи правила засобу форматування.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

`string`

Рядок для аналізу числа.

`type`

Використовуваний [тип форматирования](class.numberformatter.md#intl.numberformatter-constants.types). За замовчуванням використовується **`NumberFormatter::TYPE_DOUBLE`**

`offset`

Зміщення у рядку, з якого починається синтаксичний аналіз. При поверненні це значення міститиме усунення, у якому закінчився синтаксичний аналіз.

### Значення, що повертаються

Значення аналізованого числа або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **numfmtparse()****

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
$num = "1.234.567,891";
echo numfmt_parse($fmt, $num)."\n";
echo numfmt_parse($fmt, $num, NumberFormatter::TYPE_INT32)."\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
$num = "1.234.567,891";
echo $fmt->parse($num)."\n";
echo $fmt->parse($num, NumberFormatter::TYPE_INT32)."\n";
?>
```

Результат виконання цього прикладу:

```
1234567.891
1234567
```

### Дивіться також

-   [numfmtgeterrorcode()](numberformatter.geterrorcode.md) - Отримує останній код помилки засобу форматування
-   [numfmtformat()](numberformatter.format.md) - Форматує число
-   [numfmtparsecurrency()](numberformatter.parsecurrency.md) - Розбирає номер валюти
