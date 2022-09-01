---
navigation:
  - dateperiod.getdateinterval.md: '« DatePeriod::getDateInterval'
  - dateperiod.getrecurrences.md: 'DatePeriod::getRecurrences »'
  - index.md: PHP Manual
  - class.dateperiod.md: DatePeriod
title: 'DatePeriod::getEndDate'
---
# DatePeriod::getEndDate

(PHP 5> = 5.6.5, PHP 7, PHP 8)

DatePeriod::getEndDate — Повертає кінцеву дату періоду

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DatePeriod::getEndDate(): ?DateTimeInterface
```

Повертає кінцеву дату періоду.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`null`**, якщо [DatePeriod](class.dateperiod.md) не містить кінцевої дати. Наприклад, при ініціалізації з параметром `recurrences` або `isostr` без зазначення кінцевої дати.

Повертає об'єкт [DateTimeImmutable](class.datetimeimmutable.md), коли [DatePeriod](class.dateperiod.md) ініціалізований з об'єктом [DateTimeImmutable](class.datetimeimmutable.md) як параметр `end`

В іншому випадку повертає клонований об'єкт (object) [DateTime](class.datetime.md), що представляє дату закінчення.

### Приклади

**Приклад #1 Приклад використання **DatePeriod::getEndDate()****

```php
<?php
$period = new DatePeriod(
    new DateTime('2016-05-16T00:00:00Z'),
    new DateInterval('P1D'),
    new DateTime('2016-05-20T00:00:00Z')
);
$start = $period->getEndDate();
echo $start->format(DateTime::ISO8601);
?>
```

Результат виконання даних прикладів:

```
2016-05-20T00:00:00+0000
```

**Приклад #2 Приклад використання **DatePeriod::getEndDate()** без дати закінчення**

```php
<?php
$period = new DatePeriod(
    new DateTime('2016-05-16T00:00:00Z'),
    new DateInterval('P1D'),
    7
);
var_dump($period->getEndDate());
?>
```

Результат виконання цього прикладу:

```
NULL
```

### Дивіться також

-   [DatePeriod::getStartDate()](dateperiod.getstartdate.md) - Повертає початкову дату періоду
-   [DatePeriod::getDateInterval()](dateperiod.getdateinterval.md) - Повертає інтервал
