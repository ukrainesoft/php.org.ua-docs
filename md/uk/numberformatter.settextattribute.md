---
navigation:
  - numberformatter.setsymbol.md: '« NumberFormatter::setSymbol'
  - class.locale.md: Locale »
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::setTextAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# NumberFormatter::setTextAttribute

# numfmt\_set\_text\_attribute

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::setTextAttribute -- numfmt\_set\_text\_attribute — Встановлює текстовий атрибут

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::setTextAttribute(int $attribute, string $value): bool
```

Процедурний стиль

```methodsynopsis
numfmt_set_text_attribute(NumberFormatter $formatter, int $attribute, string $value): bool
```

Встановлює текстовий атрибут, пов'язаний із засобом форматування. Приклад текстового атрибута є суфікс для позитивних чисел. Якщо засіб форматування не розуміє атрибут, видається помилка **`U_UNSUPPORTED_ERROR`**Средства форматирования на основе правил понимают только**`NumberFormatter::DEFAULT_RULESET`**и**`NumberFormatter::PUBLIC_RULESETS`**

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

`attribute`

Спецификатор атрибута - одна из констант[текстового атрибуту](class.numberformatter.md#intl.numberformatter-constants.unumberformattextattribute)

`value`

Текст значення атрибута.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**numfmt\_set\_text\_attribute()\*\*\*\*

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Префикс: ".numfmt_get_text_attribute($fmt, NumberFormatter::NEGATIVE_PREFIX)."\n";
echo numfmt_format($fmt, -1234567.891234567890000)."\n";
numfmt_set_text_attribute($fmt, NumberFormatter::NEGATIVE_PREFIX, "MINUS");
echo "Префикс: ".numfmt_get_text_attribute($fmt, NumberFormatter::NEGATIVE_PREFIX)."\n";
echo numfmt_format($fmt, -1234567.891234567890000)."\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Префикс: ".$fmt->getTextAttribute(NumberFormatter::NEGATIVE_PREFIX)."\n";
echo $fmt->format(-1234567.891234567890000)."\n";
$fmt->setTextAttribute(NumberFormatter::NEGATIVE_PREFIX, "MINUS");
echo "Префикс: ".$fmt->getTextAttribute(NumberFormatter::NEGATIVE_PREFIX)."\n";
echo $fmt->format(-1234567.891234567890000)."\n";
?>
```

Результат виконання наведеного прикладу:

```
Префикс: -
-1.234.567,891
Префикс: MINUS
MINUS1.234.567,891
```

### Дивіться також

-   [numfmt\_get\_error\_code()](numberformatter.geterrorcode.md) \- Отримує останній код помилки засобу форматування
-   [numfmt\_get\_text\_attribute()](numberformatter.gettextattribute.md) \- Отримує текстовий атрибут
-   [numfmt\_set\_attribute()](numberformatter.setattribute.md) \- Встановлює атрибут
