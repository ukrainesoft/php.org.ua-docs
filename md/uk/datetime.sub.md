Змінює вказаний об'єкт DateTime, віднімаючи вказаний об'єкт DateInterval.

-   [« DateTime::setTimezone](datetime.settimezone.html)
    
-   [DateTimeImmutable »](class.datetimeimmutable.html)
    
-   [PHP Manual](index.html)
    
-   [DateTime](class.datetime.html)
    
-   Змінює вказаний об'єкт DateTime, віднімаючи вказаний об'єкт DateInterval.
    

# DateTime::sub

# datesub

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateTime::sub -- datesub — Змінює вказаний об'єкт DateTime, віднімаючи вказаний об'єкт [DateInterval](class.dateinterval.html)

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::sub(DateInterval $interval): DateTime
```

Процедурний стиль

```methodsynopsis
date_sub(DateTime $object, DateInterval $interval): DateTime
```

Віднімає з часу об'єкта DateTime заданий інтервал [DateInterval](class.dateinterval.html)

Подібний до методу [DateTimeImmutable::sub()](datetimeimmutable.sub.html), крім роботи з об'єктом [DateTime](class.datetime.html)

Процедурна версія приймає об'єкт [DateTime](class.datetime.html) як перший аргумент.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.html), що повертається [date\_create()](function.date-create.html). Функція змінює цей об'єкт.

`interval`

Об'єкт класу [DateInterval](class.dateinterval.html)

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.html) для застосування в ланцюгу методів або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DateTimeImmutable::sub()](datetimeimmutable.sub.html) - Віднімає передану кількість днів, місяців, років, годин, хвилин та секунд