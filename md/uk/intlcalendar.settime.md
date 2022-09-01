---
navigation:
  - intlcalendar.setskippedwalltimeoption.md: '« IntlCalendar::setSkippedWallTimeOption'
  - intlcalendar.settimezone.md: 'IntlCalendar::setTimeZone »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::setTime'
---
# IntlCalendar::setTime

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::setTime — Встановлює календарний час у мілісекундах з початку епохи Unix

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::setTime(float $timestamp): bool
```

Процедурний стиль

```methodsynopsis
intlcal_set_time(IntlCalendar $calendar, float $timestamp): bool
```

Встановлює момент, наданий об'єктом. Момент представлений числом з плаваючою точкою (float), значення якого має бути цілим числом мілісекунд, що пройшли з початку епохи Unix (1 січня 1970 00:00:00.000 UTC), без урахування додаткових секунд. Усі значення полів будуть відповідно перераховані.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`timestamp`

Момент, представлений кількістю мілісекунд між цим моментом та епохою Unix, без урахування додаткових секунд.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::setTime()****

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'fr_FR');

$cal = new IntlGregorianCalendar(2013, 5 /* May */, 1, 12, 0, 0);

echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";

/* В Europe/Lisbon 27 октября 2013 года в 02:00 часы переводятся на один час назад,
   а часовой пояс - с UTC+01 на UTC+00 */

$cal->setTime(strtotime('2013-10-27 00:30:00 UTC') * 1000.);

echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";

$cal->setTime(strtotime('2013-10-27 01:30:00 UTC') * 1000.);

echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";
```

Результат виконання цього прикладу:

```
samedi 1 juin 2013 12:00:00 heure avancée d’Europe de l’Ouest
dimanche 27 octobre 2013 01:30:00 heure avancée d’Europe de l’Ouest
dimanche 27 octobre 2013 01:30:00 heure normale d’Europe de l’Ouest
```
