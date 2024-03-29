---
navigation:
  - datetimeimmutable.setdate.md: '« DateTimeImmutable::setDate'
  - datetimeimmutable.settime.md: 'DateTimeImmutable::setTime »'
  - index.md: PHP Manual
  - class.datetimeimmutable.md: DateTimeImmutable
title: 'DateTimeImmutable::setISODate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTimeImmutable::setISODate

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

DateTimeImmutable::setISODate — Встановлює дату у форматі ISO

### Опис

```methodsynopsis
public DateTimeImmutable::setISODate(int $year, int $week, int $dayOfWeek = 1): DateTimeImmutable
```

Повертає новий об'єкт DateTimeImmutable з датою, встановленою відповідно до стандарту ISO 8601 - з використанням усунення тижнів та днів, а не конкретних дат.

### Список параметрів

`year`

Рік дати.

`week`

Тиждень дати.

`dayOfWeek`

Зміщення з першого дня тижня.

### Значення, що повертаються

Повертає новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md) із модифікованими даними.

### Приклади

**Приклад #1 Приклад використання** DateTimeImmutable::setISODate()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable();

$date->setISODate(2008, 2);
echo $date->format('Y-m-d') . "\n";

$date->setISODate(2008, 2, 7);
echo $date->format('Y-m-d') . "\n";
?>
```

Процедурний стиль

```php
<?php
$date = date_create();

date_isodate_set($date, 2008, 2);
echo date_format($date, 'Y-m-d') . "\n";

date_isodate_set($date, 2008, 2, 7);
echo date_format($date, 'Y-m-d') . "\n";
?>
```

Результат виконання наведених прикладів:

```
2008-01-07
2008-01-13
```

**Приклад #2 Значення, що виходять за межі діапазону, додаються до батьківських значень**

```php
<?php
$date = new DateTimeImmutable();

$newDate = $date->setISODate(2008, 2, 7);
echo $newDate->format('Y-m-d') . "\n";

$newDate = $date->setISODate(2008, 2, 8);
echo $newDate->format('Y-m-d') . "\n";

$newDate = $date->setISODate(2008, 53, 7);
echo $newDate->format('Y-m-d') . "\n";
?>
```

Результат виконання наведеного прикладу:

```
2008-01-13
2008-01-14
2009-01-04
```

**Приклад #3 Пошук місяця, в якому знаходиться тиждень**

```php
<?php
$date = new DateTimeImmutable();
$newDate = $date->setISODate(2008, 14);
echo $newDate->format('n');
?>
```

Результат виконання наведених прикладів:

```
3
```

### Дивіться також

-   [DateTimeImmutable::setDate()](datetimeimmutable.setdate.md) \- Встановлює дату
-   [DateTimeImmutable::setTime()](datetimeimmutable.settime.md) \- Встановлює час
