Повертає новий об'єкт із доданою кількістю днів, місяців, років, годин, хвилин та секунд

-   [« DateTimeImmutable](class.datetimeimmutable.md)
    
-   [DateTimeImmutable::construct »](datetimeimmutable.construct.md)
    
-   [PHP Manual](index.md)
    
-   [DateTimeImmutable](class.datetimeimmutable.md)
    
-   Повертає новий об'єкт із доданою кількістю днів, місяців, років, годин, хвилин та секунд
    

# DateTimeImmutable::add

(PHP 5> = 5.5.0, PHP 7, PHP 8)

DateTimeImmutable::add — Повертає новий об'єкт із доданою кількістю днів, місяців, років, годин, хвилин та секунд

### Опис

```methodsynopsis
public DateTimeImmutable::add(DateInterval $interval): DateTimeImmutable
```

Створює новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md) та додає до нього вказаний об'єкт [DateInterval](class.dateinterval.md) для уявлення нового значення.

### Список параметрів

`interval`

Об'єкт [DateInterval](class.dateinterval.md)

### Значення, що повертаються

Повертає новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md) з модифікованими даними або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **DateTimeImmutable::add()****

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable('2000-01-01');
$newDate = $date->add(new DateInterval('P10D'));
echo $newDate->format('Y-m-d') . "\n";
?>
```

**Приклад #2 Додатковий приклад використання **DateTimeImmutable::add()****

```php
<?php
$date = new DateTimeImmutable('2000-01-01');
$newDate = $date->add(new DateInterval('PT10H30S'));
echo $newDate->format('Y-m-d H:i:s') . "\n";

$date = new DateTimeImmutable('2000-01-01');
$newDate = $date->add(new DateInterval('P7Y5M4DT4H3M2S'));
echo $newDate->format('Y-m-d H:i:s') . "\n";
?>
```

Результат виконання цього прикладу:

```
2000-01-01 10:00:30
2007-06-05 04:03:02
```

**Приклад #3 Будьте обережні при додаванні місяців**

```php
<?php
$date = new DateTimeImmutable('2000-12-31');
$interval = new DateInterval('P1M');

$newDate1 = $date->add($interval);
echo $newDate1->format('Y-m-d') . "\n";

$newDate2 = $newDate1->add($interval);
echo $newDate2->format('Y-m-d') . "\n";
?>
```

Результат виконання цього прикладу:

```
2001-01-31
2001-03-03
```

### Дивіться також

-   [DateTimeImmutable::sub()](datetimeimmutable.sub.md) - Віднімає передану кількість днів, місяців, років, годин, хвилин та секунд
-   [DateTimeImmutable::diff()](datetime.diff.md) - Повертає різницю між двома об'єктами DateTime
-   [DateTimeImmutable::modify()](datetimeimmutable.modify.md) - Створює новий об'єкт із зміненою тимчасовою міткою