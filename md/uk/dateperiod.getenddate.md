Повертає кінцеву дату періоду

-   [« DatePeriod::getDateInterval](dateperiod.getdateinterval.html)
    
-   [DatePeriod::getRecurrences »](dateperiod.getrecurrences.html)
    
-   [PHP Manual](index.html)
    
-   [DatePeriod](class.dateperiod.html)
    
-   Повертає кінцеву дату періоду
    

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

Повертає **`null`**, якщо [DatePeriod](class.dateperiod.html) не містить кінцевої дати. Наприклад, при ініціалізації з параметром `recurrences` або `isostr` без зазначення кінцевої дати.

Повертає об'єкт [DateTimeImmutable](class.datetimeimmutable.html), коли [DatePeriod](class.dateperiod.html) ініціалізований з об'єктом [DateTimeImmutable](class.datetimeimmutable.html) як параметр `end`

В іншому випадку повертає клонований об'єкт (object) [DateTime](class.datetime.html), що представляє дату закінчення.

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

-   [DatePeriod::getStartDate()](dateperiod.getstartdate.html) - Повертає початкову дату періоду
-   [DatePeriod::getDateInterval()](dateperiod.getdateinterval.html) - Повертає інтервал