---
navigation:
  - numberformatter.setsymbol.md: '« NumberFormatter::setSymbol'
  - class.locale.md: Locale »
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::setTextAttribute'
---
# NumberFormatter::setTextAttribute

# numfmtsettextattribute

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::setTextAttribute -- numfmtsettextattribute — Встановлює текстовий атрибут

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::setTextAttribute(int $attribute, string $value): bool
```

Процедурний стиль

```methodsynopsis
numfmt_set_text_attribute(NumberFormatter $formatter, int $attribute, string $value): bool
```

Встановлює текстовий атрибут, пов'язаний із засобом форматування. Приклад текстового атрибута є суфікс для позитивних чисел. Якщо засіб форматування не розуміє атрибут, видається помилка **`U_UNSUPPORTED_ERROR`**. Засоби форматування на основі правил розуміють лише **`NumberFormatter::DEFAULT_RULESET`** і **`NumberFormatter::PUBLIC_RULESETS`**

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

`attribute`

Специфікатор атрибуту - одна з констант [текстового атрибуту](class.numberformatter.md#intl.numberformatter-constants.unumberformattextattribute)

`value`

Текст значення атрибута.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **numfmtsettextattribute()****

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Префикс: ".numfmt_get_text_attribute($fmt, NumberFormatter::NEGATIVE_PREFIX)."\n";
echo numfmt_format($fmt, -1234567.891234567890000)."\n";
numfmt_set_text_attribute($fmt, NumberFormatter::NEGATIVE_PREFIX, "MINUS");
echo "Префикс: ".numfmt_get_text_attribute($fmt, NumberFormatter::NEGATIVE_PREFIX)."\n";
echo numfmt_format($fmt, -1234567.891234567890000)."\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Префикс: ".$fmt->getTextAttribute(NumberFormatter::NEGATIVE_PREFIX)."\n";
echo $fmt->format(-1234567.891234567890000)."\n";
$fmt->setTextAttribute(NumberFormatter::NEGATIVE_PREFIX, "MINUS");
echo "Префикс: ".$fmt->getTextAttribute(NumberFormatter::NEGATIVE_PREFIX)."\n";
echo $fmt->format(-1234567.891234567890000)."\n";
?>
```

Результат виконання цього прикладу:

```
Префикс: -
-1.234.567,891
Префикс: MINUS
MINUS1.234.567,891
```

### Дивіться також

-   [numfmtgeterrorcode()](numberformatter.geterrorcode.md) - Отримує останній код помилки засобу форматування
-   [numfmtgettextattribute()](numberformatter.gettextattribute.md) - Отримує текстовий атрибут
-   [numfmtsetattribute()](numberformatter.setattribute.md) - Встановлює атрибут
