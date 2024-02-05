---
navigation:
  - datetime.construct.md: '« DateTime::\_\_construct'
  - datetime.createfromimmutable.md: 'DateTime::createFromImmutable »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::createFromFormat'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTime::createFromFormat

# date\_create\_from\_format

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DateTime::createFromFormat -- date\_create\_from\_format — Розбирає рядок з датою згідно з вказаним форматом

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

Подобен методу[DateTimeImmutable::createFromFormat()](datetimeimmutable.createfromformat.md) та функції [date\_create\_immutable\_from\_format()](function.date-create-immutable-from-format.md), але створює об'єкт [DateTime](class.datetime.md)

Цей метод, включаючи параметри, приклади та думки, документований на сторінці [DateTimeImmutable::createFromFormat](datetimeimmutable.createfromformat.md)

### Список параметрів

Дивіться параметри та їх опис на сторінці методу [DateTimeImmutable::createFromFormat](datetimeimmutable.createfromformat.md)

### Значення, що повертаються

Повертає створений екземпляр класу DateTime або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Функція викидає [ValueError](class.valueerror.md), якщо параметр `datetime` містить нульові байти.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.21, 8.1.8, 8.2.0 | Тепер при передачі нульових байтів у параметр `datetime` викидається [ValueError](class.valueerror.md), Який раніше мовчки ігнорувався. |

### Приклади

Великий набір прикладів дивіться на сторінці [DateTimeImmutable::createFromFormat](datetimeimmutable.createfromformat.md)

### Дивіться також

-   [DateTimeImmutable::createFromFormat()](datetimeimmutable.createfromformat.md) \- Розбирає рядок з датою згідно з вказаним форматом
