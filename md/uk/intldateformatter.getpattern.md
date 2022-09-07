---
navigation:
  - intldateformatter.getlocale.md: '« IntlDateFormatter::getLocale'
  - intldateformatter.gettimetype.md: 'IntlDateFormatter::getTimeType »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::getPattern'
---
# IntlDateFormatter::getPattern

# datefmtgetpattern

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getPattern -- datefmtgetpattern — Отримує шаблон, який використовується IntlDateFormatter

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getPattern(): string|false
```

Процедурний стиль

```methodsynopsis
datefmt_get_pattern(IntlDateFormatter $formatter): string|false
```

Отримує шаблон, який використовується засобом форматування.

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

Рядок шаблону, що використовується для форматування/розбору або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **datefmtgetpattern()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'Шаблон средства форматирования : ' . datefmt_get_pattern($fmt);
echo 'Первый отформатированный вывод с шаблоном ' . datefmt_format($fmt, 0);
datefmt_set_pattern($fmt,'yyyymmdd hh:mm:ss z');
echo 'Теперь шаблон средства форматирования : ' . datefmt_get_pattern($fmt);
echo 'Второй отформатированный вывод с шаблоном ' . datefmt_format($fmt, 0);

?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'Шаблон средства форматирования : ' . $fmt->getPattern();
echo 'Первый отформатированный вывод с шаблоном ' . $fmt->format(0);
$fmt->setPattern('yyyymmdd hh:mm:ss z');
echo 'Теперь шаблон средства форматирования : ' . $fmt->getPattern();
echo 'Второй отформатированный вывод с шаблоном ' . $fmt->format(0);
?>
```

Результат виконання цього прикладу:

```
Шаблон средства форматирования : MM/dd/yyyy
Первый отформатированный вывод с шаблоном 12/31/1969
Теперь шаблон средства форматирования : yyyymmdd hh:mm:ss z
Второй отформатированный вывод с шаблоном 19690031 04:00:00 PST
```

### Дивіться також

-   [datefmtsetpattern()](intldateformatter.setpattern.md) - Встановлює шаблон, який використовується IntlDateFormatter
-   [datefmtcreate()](intldateformatter.create.md) - Створює засіб форматування дати
