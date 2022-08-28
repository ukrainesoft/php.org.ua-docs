Встановлює день, який є початком тижня

-   [« IntlCalendar::set](intlcalendar.set.html)
    
-   [IntlCalendar::setLenient »](intlcalendar.setlenient.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Встановлює день, який є початком тижня
    

# IntlCalendar::setFirstDayOfWeek

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::setFirstDayOfWeek — Встановлює день, який є початком тижня

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::setFirstDayOfWeek(int $dayOfWeek): bool
```

Процедурний стиль

```methodsynopsis
intlcal_set_first_day_of_week(IntlCalendar $calendar, int $dayOfWeek): bool
```

Визначає день тижня, що вважається початком тижня. Це впливає на поведінку полів, які залежать від концепції початку та кінця тижня, наприклад: **`IntlCalendar::FIELD_WEEK_OF_YEAR`** і **`IntlCalendar::FIELD_YEAR_WOY`**

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`dayOfWeek`

Одна з констант **`IntlCalendar::DOW_SUNDAY`** **`IntlCalendar::DOW_MONDAY`** **`IntlCalendar::DOW_SATURDAY`**

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::setFirstDayOfWeek()****

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'es_ES');

$cal = IntlCalendar::createInstance();
$cal->set(2013, 5 /* Июнь */, 30); // Воскресенье

var_dump($cal->getFirstDayOfWeek()); // 2 (Понедельник)

echo IntlDateFormatter::formatObject($cal, <<<EOD
'местный день недели: 'cc'
неделя месяца    : 'W'
неделя года     : 'ww
EOD
), "\n";

$cal->setFirstDayOfWeek(IntlCalendar::DOW_SUNDAY);

echo IntlDateFormatter::formatObject($cal, <<<EOD
'местный день недели: 'cc'
неделя месяца    : 'W'
неделя года     : 'ww
EOD
), "\n";
```

Результат виконання цього прикладу:

```
int(2)
местный день недели: 7
неделя месяца    : 4
неделя года     : 26
местный день недели: 1
неделя месяца    : 5
неделя года     : 27
```