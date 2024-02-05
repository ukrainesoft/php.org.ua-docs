---
navigation:
  - dateperiod.getenddate.md: '« DatePeriod::getEndDate'
  - dateperiod.getstartdate.md: 'DatePeriod::getStartDate »'
  - index.md: PHP Manual
  - class.dateperiod.md: DatePeriod
title: 'DatePeriod::getRecurrences'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DatePeriod::getRecurrences

(PHP 7 >= 7.2.17/7.3.4, PHP 8)

DatePeriod::getRecurrences — Отримує кількість повторів

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DatePeriod::getRecurrences(): ?int
```

Отримує кількість повторів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість повторень, задану шляхом явної передачі параметра `$recurrences` у конструктор класу [DatePeriod](class.dateperiod.md)или\*\*`null`\*\* в іншому випадку.

### Приклади

**Приклад #1 Різні значення для **DatePeriod::getRecurrences()****

```php
<?php

$start = new DateTime('2018-12-31 00:00:00');
$end   = new DateTime('2021-12-31 00:00:00');
$interval = new DateInterval('P1M');
$recurrences = 5;

// повторения, явно заданные в конструкторе
$period = new DatePeriod($start, $interval, $recurrences, DatePeriod::EXCLUDE_START_DATE);
echo $period->getRecurrences(), "\n";

$period = new DatePeriod($start, $interval, $recurrences);
echo $period->getRecurrences(), "\n";

$period = new DatePeriod($start, $interval, $recurrences, DatePeriod::INCLUDE_END_DATE);
echo $period->getRecurrences(), "\n\n";

// повторения, не заданные в конструкторе
$period = new DatePeriod($start, $interval, $end);
var_dump($period->getRecurrences());

$period = new DatePeriod($start, $interval, $end, DatePeriod::EXCLUDE_START_DATE);
var_dump($period->getRecurrences());
?>
```

Результат виконання наведеного прикладу:

5  
5

NULL  
NULL

### Дивіться також

-   [DatePeriod::$recurrences](class.dateperiod.md#dateperiod.props.recurrences)
