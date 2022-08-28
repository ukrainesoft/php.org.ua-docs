Перетворює IntlCalendar на об'єкт DateTime

-   [« IntlCalendar::setTimeZone](intlcalendar.settimezone.html)
    
-   [IntlGregorianCalendar »](class.intlgregoriancalendar.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Перетворює IntlCalendar на об'єкт DateTime
    

# IntlCalendar::toDateTime

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a2)

IntlCalendar::toDateTime — Перетворює IntlCalendar на об'єкт DateTime

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::toDateTime(): DateTime|false
```

Процедурний стиль

```methodsynopsis
intlcal_to_date_time(IntlCalendar $calendar): DateTime|false
```

Створює об'єкт [DateTime](class.datetime.html), який представляє той же момент (з точністю до секунди, з помилкою округлення менше 1 секунди) з аналогічним часовим поясом (різниця в тому, що часовий пояс [DateTime](class.datetime.html) підтримується часовим поясом PHP, у той час як часовий пояс [IntlCalendar](class.intlcalendar.html) підтримується ICU).

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

### Значення, що повертаються

Об'єкт [DateTime](class.datetime.html) з тим же часовим поясом, що і заданий об'єкт (хоча з використанням бази даних PHP замість ICU) і з тим самим часом, за винятком меншої точності (друга точність замість мілісекунд). Повертає **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::toDateTime()****

```php
<?php
ini_set('date.timezone', 'UTC');
ini_set('intl.default_locale', 'pt_PT');

$cal = IntlCalendar::createInstance('Europe/Lisbon'); //current time

$dt = $cal->toDateTime();
print_r($dt);
```

Результат виконання цього прикладу:

```
DateTime Object
(
    [date] => 2013-07-02 00:29:13
    [timezone_type] => 3
    [timezone] => Europe/Lisbon
)
```

### Дивіться також

-   [IntlCalendar::fromDateTime()](intlcalendar.fromdatetime.html) - Створює IntlCalendar з об'єкта чи рядка DateTime
-   [IntlCalendar::getTime()](intlcalendar.gettime.html) - Отримує час, представлений на даний момент об'єктом
-   [IntlCalendar::createInstance()](intlcalendar.createinstance.html) - Створює новий об'єкт IntlCalendar
-   [DateTime::\_\_construct()](datetime.construct.html) - Конструктор класу DateTime