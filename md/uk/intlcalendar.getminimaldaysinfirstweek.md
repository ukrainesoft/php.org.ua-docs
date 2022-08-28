Отримує мінімальну кількість днів, яка може бути в першому тижні на рік або місяць

-   [« IntlCalendar::getMaximum](intlcalendar.getmaximum.html)
    
-   [IntlCalendar::getMinimum »](intlcalendar.getminimum.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Отримує мінімальну кількість днів, яка може бути в першому тижні на рік або місяць
    

# IntlCalendar::getMinimalDaysInFirstWeek

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getMinimalDaysInFirstWeek — Отримує мінімальну кількість днів, яка може бути в першому тижні на рік або місяць

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getMinimalDaysInFirstWeek(): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_minimal_days_in_first_week(IntlCalendar $calendar): int|false
```

Повертає найменшу кількість днів, які мають пройти у перший тиждень року чи місяця у новому році чи місяці. Наприклад, у григоріанському календарі, якщо це значення дорівнює 1, то перший тиждень року обов'язково включатиме 1 січня, а якщо це значення дорівнює 7, то тиждень з 1 січня буде першим тижнем року, тільки якщо день тижня 1 січня збігається з днем ​​тижня, повертається [IntlCalendar::getFirstDayOfWeek()](intlcalendar.getfirstdayofweek.html); інакше це буде останній тиждень минулого року.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

### Значення, що повертаються

Ціле число (int, що представляє кількість днів або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::getMinimalDaysInFirstWeek()****

```php
<?php
ini_set('date.timezone', 'UTC');
ini_set('intl.default_locale', 'en_US');

$cal = new IntlGregorianCalendar(2013, 0 /* Январь */, 2);
var_dump(IntlDateFormatter::formatObject($cal, 'cccc')); // Среда

var_dump($cal->getMinimalDaysInFirstWeek(), // 1
$cal->getFirstDayofWeek()); // 1 (Воскресенье)

// Первая неделя 2013 года
var_dump(IntlDateFormatter::formatObject($cal, "'Week 'w' of 'Y"));

$cal->setMinimalDaysInFirstWeek(4);
// Всё ещё первая неделя 2013 года (в 1-й неделе 5 дней в новом году)
var_dump(IntlDateFormatter::formatObject($cal, "'Week 'w' of 'Y"));

$cal->setMinimalDaysInFirstWeek(6);
// 53 неделя 2012 года
var_dump(IntlDateFormatter::formatObject($cal, "'Week 'w' of 'Y"));
```

Результат виконання цього прикладу:

```
string(9) "Wednesday"
int(1)
int(1)
string(14) "Week 1 of 2013"
string(14) "Week 1 of 2013"
string(15) "Week 53 of 2012"
```