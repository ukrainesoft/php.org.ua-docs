Створює засіб форматування чисел

-   [« NumberFormatter](class.numberformatter.html)
    
-   [NumberFormatter::formatCurrency »](numberformatter.formatcurrency.html)
    
-   [PHP Manual](index.html)
    
-   [NumberFormatter](class.numberformatter.html)
    
-   Створює засіб форматування чисел
    

# NumberFormatter::create

# numfmtcreate

# NumberFormatter::construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::create -- numfmtcreate -- NumberFormatter::construct — Створює засіб форматування чисел

### Опис

Об'єктно-орієнтований стиль (метод)

```methodsynopsis
public static NumberFormatter::create(string $locale, int $style, ?string $pattern = null): ?NumberFormatter
```

Процедурний стиль

```methodsynopsis
numfmt_create(string $locale, int $style, ?string $pattern = null): ?NumberFormatter
```

Об'єктно-орієнтований стиль (конструктор):

public **NumberFormatter::construct**(string `$locale`, int `$style`, ?string `$pattern` **`null`**

Створює засіб форматування чисел.

### Список параметрів

`locale`

Локаль, у якій буде відформатовано число (назва локалі, наприклад, enCA).

`style`

Стиль форматування, одна з констант [стиля форматирования](class.numberformatter.html#intl.numberformatter-constants.unumberformatstyle). Якщо передано **`NumberFormatter::PATTERN_DECIMAL`** або **`NumberFormatter::PATTERN_RULEBASED`**, то формат числа відкривається з використанням даного шаблону, який повинен відповідати синтаксису, описаному в [» документации ICU DecimalFormat](http://www.icu-project.org/apiref/icu4c/classDecimalFormat.html#details) або [» документации ICU RuleBasedNumberFormat](http://www.icu-project.org/apiref/icu4c/classRuleBasedNumberFormat.html#details)відповідно.

`pattern`

Рядок шаблону, якщо для вибраного стилю потрібний шаблон.

### Значення, що повертаються

Повертає об'єкт [NumberFormatter](class.numberformatter.html) або **`null`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `pattern` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **numfmtcreate()****

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
$fmt = numfmt_create( 'it', NumberFormatter::SPELLOUT );
echo numfmt_format($fmt, 1142)."\n";
?>
```

**Приклад #2 Приклад використання **NumberFormatter::create()****

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo $fmt->format(1234567.891234567890000)."\n";
$fmt = new NumberFormatter( 'it', NumberFormatter::SPELLOUT );
echo $fmt->format(1142)."\n";
?>
```

Результат виконання цього прикладу:

```
1.234.567,891
millicentoquarantadue
```

### Дивіться також

-   [numfmt\_format()](numberformatter.format.html) - Форматує число
-   [numfmt\_parse()](numberformatter.parse.html) - Розбирає число