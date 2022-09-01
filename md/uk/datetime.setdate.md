---
navigation:
  - datetime.set-state.html: '« DateTime::setstate'
  - datetime.setisodate.md: 'DateTime::setISODate »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::setDate'
---
# DateTime::setDate

# datedateset

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTime::setDate -- datedateset — Встановлює дату

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::setDate(int $year, int $month, int $day): DateTime
```

Процедурний стиль

```methodsynopsis
date_date_set(    DateTime $object,    int $year,    int $month,    int $day): DateTime
```

Встановлює поточне значення дати об'єкта DateTime на нове значення.

Подібний до методу [DateTimeImmutable::setDate()](datetimeimmutable.setdate.md), крім роботи з об'єктом [DateTime](class.datetime.md) та зміною існуючого об'єкта.

Процедурна версія приймає об'єкт [DateTime](class.datetime.md) як перший аргумент.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [datecreate()](function.date-create.html). Функція змінює цей об'єкт.

`year`

Рік нової дати.

`month`

Місяць нової дати.

`day`

День нової дати.

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.md) для застосування в ланцюгу методів або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DateTimeImmutable::setDate()](datetimeimmutable.setdate.md) - Встановлює дату
