Створює новий об'єкт із зміненою тимчасовою міткою

-   [« DateTimeImmutable::getLastErrors](datetimeimmutable.getlasterrors.html)
    
-   [DateTimeImmutable::setstate »](datetimeimmutable.set-state.html)
    
-   [PHP Manual](index.html)
    
-   [DateTimeImmutable](class.datetimeimmutable.html)
    
-   Створює новий об'єкт із зміненою тимчасовою міткою
    

# DateTimeImmutable::modify

(PHP 5> = 5.5.0, PHP 7, PHP 8)

DateTimeImmutable::modify — Створює новий об'єкт із зміненою тимчасовою міткою

### Опис

```methodsynopsis
public DateTimeImmutable::modify(string $modifier): DateTimeImmutable|false
```

Створює новий об'єкт [DateTimeImmutable](class.datetimeimmutable.html) зі зміненою тимчасовою міткою. Початковий об'єкт не змінюється.

### Список параметрів

`modifier`

Рядок дати/часу. Пояснення коректних форматів наведено в розділі [Форматы даты и времени](datetime.formats.html)

### Значення, що повертаються

Повертає новий модифікований об'єкт DateTimeImmutable або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **DateTimeImmutable::modify()****

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable('2006-12-12');
$newDate = $date->modify('+1 day');
echo $newDate->format('Y-m-d');
?>
```

Результат виконання даних прикладів:

```
2006-12-13
```

**Приклад #2 Будьте обережні при складанні або відніманні місяців**

```php
<?php
$date = new DateTimeImmutable('2000-12-31');

$newDate1 = $date->modify('+1 month');
echo $newDate1->format('Y-m-d') . "\n";

$newDate2 = $newDate1->modify('+1 month');
echo $newDate2->format('Y-m-d') . "\n";
?>
```

Результат виконання цього прикладу:

```
2001-01-31
2001-03-03
```

### Дивіться також

-   [DateTimeImmutable::add()](datetimeimmutable.add.html) - Повертає новий об'єкт з доданою кількістю днів, місяців, років, годин, хвилин та секунд
-   [DateTimeImmutable::sub()](datetimeimmutable.sub.html) - Віднімає передану кількість днів, місяців, років, годин, хвилин та секунд
-   [DateTimeImmutable::setDate()](datetimeimmutable.setdate.html) - Встановлює дату
-   [DateTimeImmutable::setISODate()](datetimeimmutable.setisodate.html) - Встановлює дату у форматі ISO
-   [DateTimeImmutable::setTime()](datetimeimmutable.settime.html) - Встановлює час
-   [DateTimeImmutable::setTimestamp()](datetimeimmutable.settimestamp.html) - Встановлює дату та час на основі мітки часу Unix