Змінює об'єкт DateTime, додаючи кількість днів, місяців, років, годин, хвилин та секунд

-   [« DateTime](class.datetime.html)
    
-   [DateTime::construct »](datetime.construct.html)
    
-   [PHP Manual](index.html)
    
-   [DateTime](class.datetime.html)
    
-   Змінює об'єкт DateTime, додаючи кількість днів, місяців, років, годин, хвилин та секунд
    

# DateTime::add

# dateadd

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateTime::add -- dateadd — Змінює об'єкт DateTime, додаючи кількість днів, місяців, років, годин, хвилин та секунд

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::add(DateInterval $interval): DateTime
```

Процедурний стиль

```methodsynopsis
date_add(DateTime $object, DateInterval $interval): DateTime
```

Додає заданий об'єкт [DateInterval](class.dateinterval.html) до об'єкту [DateTime](class.datetime.html)

Подібний до методу [DateTimeImmutable::add()](datetimeimmutable.add.html), крім роботи з об'єктом [DateTime](class.datetime.html)

Процедурна версія приймає як перший аргумент об'єкт [DateTime](class.datetime.html)

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.html), що повертається [datecreate()](function.date-create.html). Функція змінює цей об'єкт.

`interval`

Об'єкт класу [DateInterval](class.dateinterval.html)

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.html) для застосування в ланцюгу методів або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DateTimeImmutable::add()](datetimeimmutable.add.html) - Повертає новий об'єкт з доданою кількістю днів, місяців, років, годин, хвилин та секунд