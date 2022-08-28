Отримує перший день тижня для стандарту календаря

-   [« IntlCalendar::getErrorMessage](intlcalendar.geterrormessage.html)
    
-   [IntlCalendar::getGreatestMinimum »](intlcalendar.getgreatestminimum.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Отримує перший день тижня для стандарту календаря
    

# IntlCalendar::getFirstDayOfWeek

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getFirstDayOfWeek — Отримує перший день тижня для стандарту мовного календаря

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getFirstDayOfWeek(): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_first_day_of_week(IntlCalendar $calendar): int|false
```

День тижня, який вважається початком тижня: або значення за промовчанням для цього мовного стандарту, або значення, встановлене за допомогою [IntlCalendar::setFirstDayOfWeek()](intlcalendar.setfirstdayofweek.html)

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

### Значення, що повертаються

Одна з констант: **`IntlCalendar::DOW_SUNDAY`** **`IntlCalendar::DOW_MONDAY`** **`IntlCalendar::DOW_SATURDAY`** або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::getFirstDayOfWeek()****

```php
<?php
ini_set('date.timezone', 'UTC');

$cal1 = IntlCalendar::createInstance(NULL, 'es_ES');
var_dump($cal1->getFirstDayOfWeek()); // Понедельник
$cal1->set(2013, 1 /* Февраль */, 3); // Воскресенье
var_dump($cal1->get(IntlCalendar::FIELD_WEEK_OF_YEAR)); // 5

$cal2 = IntlCalendar::createInstance(NULL, 'en_US');
var_dump($cal2->getFirstDayOfWeek()); // Воскресенье
$cal2->set(2013, 1 /* Февраль */, 3); // Воскресенье
var_dump($cal2->get(IntlCalendar::FIELD_WEEK_OF_YEAR)); // 6
```

Результат виконання цього прикладу:

```
int(2)
int(5)
int(1)
int(6)
```

### Дивіться також

-   [IntlCalendar::setFirstDayOfWeek()](intlcalendar.setfirstdayofweek.html) - Встановлює день, який є початком тижня