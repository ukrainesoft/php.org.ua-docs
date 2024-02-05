---
navigation:
  - dateperiod.getrecurrences.md: '« DatePeriod::getRecurrences'
  - ref.datetime.md: Функції дати та часу »
  - index.md: PHP Manual
  - class.dateperiod.md: DatePeriod
title: 'DatePeriod::getStartDate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DatePeriod::getStartDate

(PHP 5 >= 5.6.5, PHP 7, PHP 8)

DatePeriod::getStartDate — Повертає початкову дату періоду

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DatePeriod::getStartDate(): DateTimeInterface
```

Повертає початкову дату періоду.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [DateTimeImmutable](class.datetimeimmutable.md), когда[DatePeriod](class.dateperiod.md) ініціалізований об'єктом [DateTimeImmutable](class.datetimeimmutable.md) як параметр `start`

Інакше повертає об'єкт [DateTime](class.datetime.md)

### Приклади

**Пример #1 Пример использования**DatePeriod::getStartDate()\*\*\*\*

```php
<?php
$period = new DatePeriod('R7/2016-05-16T00:00:00Z/P1D');
$start = $period->getStartDate();
echo $start->format(DateTime::ISO8601);
?>
```

Результат виконання наведеного прикладу:

```
2016-05-16T00:00:00+0000
```

### Дивіться також

-   [DatePeriod::getEndDate()](dateperiod.getenddate.md) \- Повертає кінцеву дату періоду
-   [DatePeriod::getDateInterval()](dateperiod.getdateinterval.md) \- Повертає інтервал
