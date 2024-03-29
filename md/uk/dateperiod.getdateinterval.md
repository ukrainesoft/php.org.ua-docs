---
navigation:
  - dateperiod.createfromiso8601string.md: '« DatePeriod::createFromISO8601String'
  - dateperiod.getenddate.md: 'DatePeriod::getEndDate »'
  - index.md: PHP Manual
  - class.dateperiod.md: DatePeriod
title: 'DatePeriod::getDateInterval'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DatePeriod::getDateInterval

(PHP 5 >= 5.6.5, PHP 7, PHP 8)

DatePeriod::getDateInterval — Повертає інтервал

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DatePeriod::getDateInterval(): DateInterval
```

Повертає об'єкт [DateInterval](class.dateinterval.md), що представляє інтервал, використаний для створення періоду

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [DateInterval](class.dateinterval.md)

### Приклади

**Приклад #1 Приклад використання** DatePeriod::getDateInterval()\*\*\*\*

```php
<?php
$period = new DatePeriod('R7/2016-05-16T00:00:00Z/P1D');
$interval = $period->getDateInterval();
echo $interval->format('%d day');
?>
```

Результат виконання наведеного прикладу:

```
1 day
```

### Дивіться також

-   [DatePeriod::getStartDate()](dateperiod.getstartdate.md) \- Повертає початкову дату періоду
-   [DatePeriod::getEndDate()](dateperiod.getenddate.md) \- Повертає кінцеву дату періоду
