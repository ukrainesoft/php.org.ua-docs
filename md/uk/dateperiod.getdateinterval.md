Повертає інтервал

-   [« DatePeriod::construct](dateperiod.construct.html)
    
-   [DatePeriod::getEndDate »](dateperiod.getenddate.html)
    
-   [PHP Manual](index.html)
    
-   [DatePeriod](class.dateperiod.html)
    
-   Повертає інтервал
    

# DatePeriod::getDateInterval

(PHP 5> = 5.6.5, PHP 7, PHP 8)

DatePeriod::getDateInterval — Повертає інтервал

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DatePeriod::getDateInterval(): DateInterval
```

Повертає об'єкт [DateInterval](class.dateinterval.html), що представляє інтервал, використаний для створення періоду

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [DateInterval](class.dateinterval.html)

### Приклади

**Приклад #1 Приклад використання **DatePeriod::getDateInterval()****

```php
<?php
$period = new DatePeriod('R7/2016-05-16T00:00:00Z/P1D');
$interval = $period->getDateInterval();
echo $interval->format('%d day');
?>
```

Результат виконання цього прикладу:

```
1 day
```

### Дивіться також

-   [DatePeriod::getStartDate()](dateperiod.getstartdate.html) - Повертає початкову дату періоду
-   [DatePeriod::getEndDate()](dateperiod.getenddate.html) - Повертає кінцеву дату періоду