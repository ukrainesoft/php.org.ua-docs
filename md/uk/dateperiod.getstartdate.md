Повертає початкову дату періоду

-   [« DatePeriod::getRecurrences](dateperiod.getrecurrences.html)
    
-   [Функции даты и времени »](ref.datetime.html)
    
-   [PHP Manual](index.html)
    
-   [DatePeriod](class.dateperiod.html)
    
-   Повертає початкову дату періоду
    

# DatePeriod::getStartDate

(PHP 5> = 5.6.5, PHP 7, PHP 8)

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

Повертає об'єкт [DateTimeImmutable](class.datetimeimmutable.html), коли [DatePeriod](class.dateperiod.html) ініціалізований об'єктом [DateTimeImmutable](class.datetimeimmutable.html) як параметр `start`

Інакше повертає об'єкт [DateTime](class.datetime.html)

### Приклади

**Приклад #1 Приклад використання **DatePeriod::getStartDate()****

```php
<?php
$period = new DatePeriod('R7/2016-05-16T00:00:00Z/P1D');
$start = $period->getStartDate();
echo $start->format(DateTime::ISO8601);
?>
```

Результат виконання цього прикладу:

```
2016-05-16T00:00:00+0000
```

### Дивіться також

-   [DatePeriod::getEndDate()](dateperiod.getenddate.html) - Повертає кінцеву дату періоду
-   [DatePeriod::getDateInterval()](dateperiod.getdateinterval.html) - Повертає інтервал