---
navigation:
  - datetime.setdate.md: '« DateTime::setDate'
  - datetime.settime.md: 'DateTime::setTime »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::setISODate'
---
# DateTime::setISODate

# dateisodateset

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTime::setISODate -- dateisodateset — Встановлює дату ISO

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::setISODate(int $year, int $week, int $dayOfWeek = 1): DateTime
```

Процедурний стиль

```methodsynopsis
date_isodate_set(    DateTime $object,    int $year,    int $week,    int $dayOfWeek = 1): DateTime
```

Встановлення дати відповідно до стандарту ISO 8601, в якому використання тижнів та зміщення днями переважніше вказівки дати.

Подібний до методу [DateTimeImmutable::setISODate()](datetimeimmutable.setisodate.md), крім роботи з об'єктом [DateTime](class.datetime.md)

Процедурна версія приймає об'єкт [DateTime](class.datetime.md) як перший аргумент.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [datecreate()](function.date-create.md). Функція змінює цей об'єкт.

`year`

Рік нової дати.

`week`

Тиждень нової дати.

`dayOfWeek`

Усунення щодо початку тижня.

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.md) для застосування в ланцюгу методів або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DateTimeImmutable::setISODate()](datetimeimmutable.setisodate.md) - Встановлює дату у форматі ISO
