---
navigation:
  - class.dateperiod.md: « DatePeriod
  - dateperiod.getdateinterval.md: 'DatePeriod::getDateInterval »'
  - index.md: PHP Manual
  - class.dateperiod.md: DatePeriod
title: 'DatePeriod::construct'
---
# DatePeriod::construct

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DatePeriod::construct — Створює новий об'єкт DatePeriod

### Опис

public **DatePeriod::construct**  
[DateTimeInterface](class.datetimeinterface.md) `$start`  
[DateInterval](class.dateinterval.md) `$interval`  
int `$recurrences`  
int `$options`

public **DatePeriod::construct**  
[DateTimeInterface](class.datetimeinterface.md) `$start`  
[DateInterval](class.dateinterval.md) `$interval`  
[DateTimeInterface](class.datetimeinterface.md) `$end`  
int `$options`

public **DatePeriod::construct**(string `$isostr`, int `$options`

Створює новий об'єкт DatePeriod.

### Список параметрів

`start`

Початкова дата.

`interval`

Інтервал.

`recurrences`

Кількість повторень. Має бути більше `0`

`end`

Кінцева дата.

`isostr`

Рядок, що містить інтервал згідно [» спеціфікації ISO 8601](http://en.wikipedia.org/wiki/Iso8601#Repeating_intervals). Нульові входження (`R0/`) не підтримуються.

`options`

Можливе значення **`DatePeriod::EXCLUDE_START_DATE`** для виключення початкової дати із періоду.

### список змін

| Версия | Описание |
| --- | --- |
|  | `recurrences` має бути більше `0` |

### Приклади

**Приклад #1 Приклад використання DatePeriod**

```php
<?php
$start = new DateTime('2012-07-01');
$interval = new DateInterval('P7D');
$end = new DateTime('2012-07-31');
$recurrences = 4;
$iso = 'R4/2012-07-01T00:00:00Z/P7D';

// Эти периоды эквивалентны.
$period = new DatePeriod($start, $interval, $recurrences);
$period = new DatePeriod($start, $interval, $end);
$period = new DatePeriod($iso);

// При переборе экземпляра DatePeriod в цикле будут отображены все отобранные даты
// периода.
foreach ($period as $date) {
    echo $date->format('Y-m-d')."\n";
}
?>
```

Результат виконання цього прикладу:

```
2012-07-01
2012-07-08
2012-07-15
2012-07-22
2012-07-29
```

**Приклад #2 Приклад використання DatePeriod з **`DatePeriod::EXCLUDE_START_DATE`****

```php
<?php
$start = new DateTime('2012-07-01');
$interval = new DateInterval('P7D');
$end = new DateTime('2012-07-31');

$period = new DatePeriod($start, $interval, $end,
                         DatePeriod::EXCLUDE_START_DATE);

// При переборе экземпляра DatePeriod в цикле будут отображены все отобранные даты
// периода.
// Однако в этом случае 2012-07-01 не будет отображена.
foreach ($period as $date) {
    echo $date->format('Y-m-d')."\n";
}
?>
```

Результат виконання цього прикладу:

```
2012-07-08
2012-07-15
2012-07-22
2012-07-29
```

### Примітки

Незв'язкова кількість повторень, визначених у секції 4.5 ISO 8601 "Recurring time interval", не підтримується, тобто ні передача `"R/..."` в `isostr`ні **`null`** в `end`, не працюватимуть.
