Встановлює атрибут

-   [« NumberFormatter::parse](numberformatter.parse.html)
    
-   [NumberFormatter::setPattern »](numberformatter.setpattern.html)
    
-   [PHP Manual](index.html)
    
-   [NumberFormatter](class.numberformatter.html)
    
-   Встановлює атрибут
    

# NumberFormatter::setAttribute

# numfmtsetattribute

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::setAttribute -- numfmtsetattribute - Встановлює атрибут

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::setAttribute(int $attribute, int|float $value): bool
```

Процедурний стиль

```methodsynopsis
numfmt_set_attribute(NumberFormatter $formatter, int $attribute, int|float $value): bool
```

Встановлює числовий атрибут, пов'язаний із засобом форматування. Прикладом числового атрибута є кількість цілих цифр, що видаватиме засіб форматування.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.html)

`attribute`

Специфікатор атрибуту - одна з констант [числового атрибута](class.numberformatter.html#intl.numberformatter-constants.unumberformatattribute)

`value`

Значення атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **numfmtsetattribute()****

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Цифр: ".numfmt_get_attribute($fmt, NumberFormatter::MAX_FRACTION_DIGITS)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
numfmt_set_attribute($fmt, NumberFormatter::MAX_FRACTION_DIGITS, 2);
echo "Цифр: ".numfmt_get_attribute($fmt, NumberFormatter::MAX_FRACTION_DIGITS)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Цифр: ".$fmt->getAttribute(NumberFormatter::MAX_FRACTION_DIGITS)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
$fmt->setAttribute(NumberFormatter::MAX_FRACTION_DIGITS, 2);
echo "Цифр: ".$fmt->getAttribute(NumberFormatter::MAX_FRACTION_DIGITS)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
?>
```

Результат виконання цього прикладу:

```
Цифр: 3
1.234.567,891
Цифр: 2
1.234.567,89
```

### Дивіться також

-   [numfmt\_get\_error\_code()](numberformatter.geterrorcode.html) - Отримує останній код помилки засобу форматування
-   [numfmt\_get\_attribute()](numberformatter.getattribute.html) - Отримує атрибут
-   [numfmt\_set\_text\_attribute()](numberformatter.settextattribute.html) - Встановлює текстовий атрибут