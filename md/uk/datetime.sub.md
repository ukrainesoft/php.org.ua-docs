---
navigation:
  - datetime.settimezone.md: '« DateTime::setTimezone'
  - class.datetimeimmutable.md: DateTimeImmutable »
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::sub'
---
# DateTime::sub

# datesub

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateTime::sub -- datesub — Змінює вказаний об'єкт DateTime, віднімаючи вказаний об'єкт [DateInterval](class.dateinterval.md)

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::sub(DateInterval $interval): DateTime
```

Процедурний стиль

```methodsynopsis
date_sub(DateTime $object, DateInterval $interval): DateTime
```

Віднімає з часу об'єкта DateTime заданий інтервал [DateInterval](class.dateinterval.md)

Подібний до методу [DateTimeImmutable::sub()](datetimeimmutable.sub.md), крім роботи з об'єктом [DateTime](class.datetime.md)

Процедурна версія приймає об'єкт [DateTime](class.datetime.md) як перший аргумент.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [datecreate()](function.date-create.html). Функція змінює цей об'єкт.

`interval`

Об'єкт класу [DateInterval](class.dateinterval.md)

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.md) для застосування в ланцюгу методів або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DateTimeImmutable::sub()](datetimeimmutable.sub.md) - Віднімає передану кількість днів, місяців, років, годин, хвилин та секунд
