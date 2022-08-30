Встановлює часовий пояс, що використовується календарем

-   [« IntlCalendar::setTime](intlcalendar.settime.html)
    
-   [IntlCalendar::toDateTime »](intlcalendar.todatetime.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Встановлює часовий пояс, що використовується календарем
    

# IntlCalendar::setTimeZone

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::setTimeZone — Встановлює часовий пояс, який використовується календарем.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::setTimeZone(IntlTimeZone|DateTimeZone|string|null $timezone): bool
```

Процедурний стиль

```methodsynopsis
intlcal_set_time_zone(IntlCalendar $calendar, IntlTimeZone|DateTimeZone|string|null $timezone): bool
```

Визначає новий часовий пояс календаря. Час, представлений об'єктом, зберігається на шкоду значенням поля.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`timezone`

Новий часовий пояс, який використовуватиме календар. Його можна вказати такими способами:

-   Якщо **`null`**, то буде використаний часовий пояс за замовчуванням, задана в ini-налаштування [date.timezone](datetime.configuration.html#ini.date.timezone) або за допомогою функції [datedefaulttimezoneset()](function.date-default-timezone-set.html) та повернена функцією [datedefaulttimezoneget()](function.date-default-timezone-get.html)
    
-   Об'єкт класу [IntlTimeZone](class.intltimezone.html)
    
-   Об'єкт класу [DateTimeZone](class.datetimezone.html). Його ідентифікатор буде вилучено і на його основі буде створено об'єкт часового поясу ICU; часовий пояс буде збережено в базі даних ICU, а не PHP.
    
-   Рядок є коректним ідентифікатором часового поясу ICU. Дивіться [IntlTimeZone::createTimeZoneIDEnumeration()](intltimezone.createtimezoneidenumeration.html). "Сирі" усунення, типу `"GMT+08:30"`, також підтримуються.
    

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::setTimeZone()****

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'es_ES');

$cal = new IntlGregorianCalendar(2013, 5 /* May */, 1, 12, 0, 0);

echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";
echo "(instant {$cal->getTime()})\n";

$cal->setTimeZone(IntlTimeZone::getGMT());
echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";
echo "(instant {$cal->getTime()})\n";

$cal->setTimeZone('GMT+03:33');
echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";
echo "(instant {$cal->getTime()})\n";
```

Результат виконання цього прикладу:

```
sábado, 1 de junio de 2013 12:00:00 Hora de verano de Europa occidental
(instant 1370084400000)
sábado, 1 de junio de 2013 11:00:00 GMT
(instant 1370084400000)
sábado, 1 de junio de 2013 14:33:00 GMT+03:33
(instant 1370084400000)
```