---
navigation:
  - numberformatter.setattribute.md: '« NumberFormatter::setAttribute'
  - numberformatter.setsymbol.md: 'NumberFormatter::setSymbol »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::setPattern'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# NumberFormatter::setPattern

# numfmt\_set\_pattern

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::setPattern -- numfmt\_set\_pattern — Встановлює шаблон засобу форматування

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

Шаблон в синтаксисе, описанном в[» документації ICU DecimalFormat](https://unicode-org.github.io/icu-docs/apidoc/released/icu4c/classDecimalFormat.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** numfmt\_set\_pattern()\*\*\*\*

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Шаблон: ".numfmt_get_pattern($fmt)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
numfmt_set_pattern($fmt, "#0.# kg");
echo "Шаблон: ".numfmt_get_pattern($fmt)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Шаблон: ".$fmt->getPattern()."\n";
echo $fmt->format(1234567.891234567890000)."\n";
$fmt->setPattern("#0.# kg");
echo "Шаблон: ".$fmt->getPattern()."\n";
echo $fmt->format(1234567.891234567890000)."\n";
?>
```

Результат виконання наведеного прикладу:

```
Шаблон: #,##0.###
1.234.567,891
Шаблон: #0.# kg
1234567,9 kg
```

### Дивіться також

-   [numfmt\_get\_error\_code()](numberformatter.geterrorcode.md) \- Отримує останній код помилки засобу форматування
-   [numfmt\_create()](numberformatter.create.md) \- Створює засіб форматування чисел
-   [numfmt\_get\_pattern()](numberformatter.getpattern.md) \- Отримує шаблон засобу форматування
