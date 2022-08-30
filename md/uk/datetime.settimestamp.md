Встановлює дату та час на основі мітки часу Unix

-   [« DateTime::setTime](datetime.settime.html)
    
-   [DateTime::setTimezone »](datetime.settimezone.html)
    
-   [PHP Manual](index.html)
    
-   [DateTime](class.datetime.html)
    
-   Встановлює дату та час на основі мітки часу Unix
    

# DateTime::setTimestamp

# datetimestampset

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateTime::setTimestamp -- datetimestampset — Встановлює дату та час на основі мітки часу Unix

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::setTimestamp(int $timestamp): DateTime
```

Процедурний стиль

```methodsynopsis
date_timestamp_set(DateTime $object, int $timestamp): DateTime
```

Встановлює дату та час, ґрунтуючись на мітці часу Unix.

Подібний до методу [DateTimeImmutable::setTimestamp()](datetimeimmutable.settimestamp.html), крім роботи з об'єктом [DateTime](class.datetime.html)

Процедурна версія приймає об'єкт [DateTime](class.datetime.html) як перший аргумент.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.html), що повертається [datecreate()](function.date-create.html). Функція змінює цей об'єкт.

`timestamp`

Мітка часу Unix представляє дату. Встановлення позначок часу за межами діапазону цілих чисел (int) можливе при використанні [DateTimeImmutable::modify()](datetimeimmutable.modify.html) з форматом `@`

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.html) для застосування в ланцюгу методів або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DateTimeImmutable::setTimestamp()](datetimeimmutable.settimestamp.html) - Встановлює дату та час на основі мітки часу Unix