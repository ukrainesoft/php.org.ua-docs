---
navigation:
  - datetime.construct.md: '« DateTime::construct'
  - datetime.createfromimmutable.md: 'DateTime::createFromImmutable »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::createFromFormat'
---
# DateTime::createFromFormat

# datecreatefromformat

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateTime::createFromFormat -- datecreatefromformat — Розбирає рядок з датою згідно з вказаним форматом

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static DateTime::createFromFormat(string $format, string $datetime, ?DateTimeZone $timezone = null): DateTime|false
```

Процедурний стиль

```methodsynopsis
date_create_from_format(string $format, string $datetime, ?DateTimeZone $timezone = null): DateTime|false
```

Повертає новий об'єкт DateTime, що представляє дату та час, задані рядком `datetime`, яка була відформатована у зазначеному `format`

Подібний до методу [DateTimeImmutable::createFromFormat()](datetimeimmutable.createfromformat.md), крім роботи з об'єктом [DateTime](class.datetime.md)

Процедурна версія приймає об'єкт [DateTime](class.datetime.md) як перший аргумент.

### Список параметрів

Дивіться параметри та їх опис на сторінці методу [DateTimeImmutable::createFromFormat](datetimeimmutable.createfromformat.md)

### Значення, що повертаються

Повертає створений екземпляр класу DateTime або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DateTimeImmutable::createFromFormat()](datetimeimmutable.createfromformat.md) - Розбирає рядок з датою згідно з вказаним форматом
