---
navigation:
  - intldateformatter.getpattern.md: '« IntlDateFormatter::getPattern'
  - intldateformatter.gettimezoneid.md: 'IntlDateFormatter::getTimeZoneId »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::getTimeType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlDateFormatter::getTimeType

# datefmt\_get\_timetype

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getTimeType -- datefmt\_get\_timetype — Отримує тип часу, який використовується IntlDateFormatter

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getTimeType(): int|false
```

Процедурний стиль

```methodsynopsis
datefmt_get_timetype(IntlDateFormatter $formatter): int|false
```

Повертає тип часу, який використовується засобом форматування.

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

Значення поточного [типу дати](class.intldateformatter.md#intl.intldateformatter-constants)средства форматирования или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** datefmt\_get\_timetype()\*\*\*\*

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Тип времени средства форматирования : ' . datefmt_get_timetype($fmt);
echo 'Первый отформатированный вывод ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::SHORT,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Теперь тип времени средства форматирования : ' . datefmt_get_timetype($fmt);
echo 'Второй отформатированный вывод ' . datefmt_format($fmt, 0);

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
    IntlDateFormatter::GREGORIAN
);
echo 'Тип времени средства форматирования : ' . $fmt->getTimeType();
echo 'Первый отформатированный вывод ' . $fmt->format(0);

$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::SHORT,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Теперь тип времени средства форматирования : ' . $fmt->getTimeType();
echo 'Второй отформатированный вывод ' . $fmt->format(0);

?>
```

Результат виконання наведеного прикладу:

```
Тип времени средства форматирования : 0
Первый отформатированный вывод Wednesday, December 31, 1969 4:00:00 PM PT
Теперь тип времени средства форматирования : 3
Второй отформатированный вывод Wednesday, December 31, 1969 4:00 PM
```

### Дивіться також

-   [datefmt\_get\_datetype()](intldateformatter.getdatetype.md) \- Отримує тип дати, що використовується IntlDateFormatter
-   [datefmt\_create()](intldateformatter.create.md) \- Створює засіб форматування дати
