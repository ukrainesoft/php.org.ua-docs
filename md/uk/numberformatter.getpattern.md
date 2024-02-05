---
navigation:
  - numberformatter.getlocale.md: '« NumberFormatter::getLocale'
  - numberformatter.getsymbol.md: 'NumberFormatter::getSymbol »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::getPattern'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# NumberFormatter::getPattern

# numfmt\_get\_pattern

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::getPattern -- numfmt\_get\_pattern — Отримує шаблон засобу форматування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::getPattern(): string|false
```

Процедурний стиль

```methodsynopsis
numfmt_get_pattern(NumberFormatter $formatter): string|false
```

Витягує шаблон, який використовується засобом форматування.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

### Значення, що повертаються

Рядок (string) шаблону, що використовується засобом форматування або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**numfmt\_get\_pattern()\*\*\*\*

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
-   [numfmt\_set\_pattern()](numberformatter.setpattern.md) \- Встановлює шаблон засобу форматування
-   [numfmt\_create()](numberformatter.create.md) \- Створює засіб форматування чисел
