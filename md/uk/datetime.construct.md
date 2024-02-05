---
navigation:
  - datetime.add.md: '« DateTime::add'
  - datetime.createfromformat.md: 'DateTime::createFromFormat »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTime::\_\_construct

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

DateTime::\_\_construct - Конструктор класу DateTime

### Опис

public**DateTime::\_\_construct**(string`$datetime` = "now", ?[DateTimeZone](class.datetimezone.md) `$timezone` **`null`**) .

Цей конструктор схожий на конструктор [DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md), але працює з об'єктом [DateTime](class.datetime.md). Врахуйте, що замість цього класу краще працювати із класом [DateTimeImmutable](class.datetimeimmutable.md) та його функціями.

Повертає новий об'єкт DateTime.

### Список параметрів

`datetime`

Рядок дати/часу. Пояснення коректних форматів наведено в розділі [Формати дати та часу](datetime.formats.md)

Якщо використовується аргумент `$timezone`, то для отримання поточного часу в новому об'єкті достатньо передати `"now"` як цей аргумент.

`timezone`

Об'єкт класу [DateTimeZone](class.datetimezone.md), представляющий часовой пояс параметра`$datetime`

Якщо аргумент `$timezone`не задан или\*\*`null`\*\*, буде використано поточний часовий пояс.

> **Зауваження** :
> 
> Значение аргумента`$timezone`, так само як і поточний часовий пояс не враховуватимуться, якщо як аргумент `$datetime` передається мітка часу UNIX (наприклад, `@946684800`) або час, у якому часовий пояс вже міститься (наприклад, `2010-01-28T15:00:00+02:00`

### Значення, що повертаються

Повертає створений об'єкт класу DateTime.

### Помилки

Якщо буде передано неприпустимий рядок дати/часу, буде викинуто виняток [DateMalformedStringException](class.datemalformedstringexception.md). До PHP 8.3 викидався виняток [Exception](class.exception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер замість винятку [Exception](class.exception.md) викидається виняток [DateMalformedStringException](class.datemalformedstringexception.md), якщо передано неприпустимий рядок. |

### Дивіться також

-   [DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md) \- Повертає новий об'єкт DateTimeImmutable
