---
navigation:
  - class.numberformatter.md: « NumberFormatter
  - numberformatter.formatcurrency.md: 'NumberFormatter::formatCurrency »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::create'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# NumberFormatter::create

# numfmt\_create

# NumberFormatter::\_\_construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::create -- numfmt\_create -- NumberFormatter::\_\_construct — Створює засіб форматування чисел

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

public**NumberFormatter::\_\_construct**(string`$locale`, int`$style`, ?string`$pattern` **`null`**) .

Створює засіб форматування чисел.

### Список параметрів

`locale`

Локаль, у якій буде відформатовано число (назва локалі, наприклад, en\_CA).

`style`

Стиль форматування, одна з констант [стилю форматування](class.numberformatter.md#intl.numberformatter-constants.unumberformatstyle). Якщо передано **`NumberFormatter::PATTERN_DECIMAL`**или**`NumberFormatter::PATTERN_RULEBASED`**, то формат числа відкривається з використанням даного шаблону, який повинен відповідати синтаксису, описаному в [» документації ICU DecimalFormat](https://unicode-org.github.io/icu-docs/apidoc/released/icu4c/classDecimalFormat.md) або [» документації ICU RuleBasedNumberFormat](https://unicode-org.github.io/icu/userguide/format_parse/numbers/rbnf.md)відповідно.

`pattern`

Рядок шаблону, якщо для вибраного стилю потрібний шаблон.

### Значення, що повертаються

Повертає об'єкт [NumberFormatter](class.numberformatter.md)или\*\*`null`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `pattern` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**numfmt\_create()\*\*\*\*

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
$fmt = numfmt_create( 'it', NumberFormatter::SPELLOUT );
echo numfmt_format($fmt, 1142)."\n";
?>
```

**Пример #2 Пример использования**NumberFormatter::create()\*\*\*\*

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo $fmt->format(1234567.891234567890000)."\n";
$fmt = new NumberFormatter( 'it', NumberFormatter::SPELLOUT );
echo $fmt->format(1142)."\n";
?>
```

Результат виконання наведеного прикладу:

```
1.234.567,891
millicentoquarantadue
```

### Дивіться також

-   [numfmt\_format()](numberformatter.format.md) \- Форматує число
-   [numfmt\_parse()](numberformatter.parse.md) \- Розбирає число
