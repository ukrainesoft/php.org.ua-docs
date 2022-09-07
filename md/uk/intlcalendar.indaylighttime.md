---
navigation:
  - intlcalendar.getweekendtransition.md: '« IntlCalendar::getWeekendTransition'
  - intlcalendar.isequivalentto.md: 'IntlCalendar::isEquivalentTo »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::inDaylightTime'
---
# IntlCalendar::inDaylightTime

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::inDaylightTime — Визначає, чи час об'єкта переходить на літній час.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::inDaylightTime(): bool
```

Процедурний стиль

```methodsynopsis
intlcal_in_daylight_time(IntlCalendar $calendar): bool
```

Визначає, чи використовує представлений цим об'єктом екземпляр та часовий пояс цього об'єкта літній час на даний момент.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо дата вказана в літній час, в іншому випадку повертає **`false`**

У разі виникнення помилки також повертається **`false`**. Для виявлення умов помилки використовуйте [intlgeterrorcode()](function.intl-get-error-code.md) або настройте викидання [исключений](intl.configuration.md#ini.intl.use-exceptions) в Intl.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::inDaylightTime()****

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'pt_PT');

$cal = new IntlGregorianCalendar(2013, 6 /* Июль */, 1, 4, 56, 31);
var_dump($cal->inDaylightTime()); // true
$cal->set(IntlCalendar::FIELD_MONTH, 11 /* Декабрь */);
var_dump($cal->inDaylightTime()); // false

//DST end transition on 2013-10-27 at 0200 (время процессора назад на 1 час)
$cal = new IntlGregorianCalendar(2013, 9 /* Октябрь */, 27, 1, 30, 0);

var_dump($cal->inDaylightTime()); // false (по умолчанию WALLTIME_LAST)

$cal->setRepeatedWallTimeOption(IntlCalendar::WALLTIME_FIRST);
$cal->set(IntlCalendar::FIELD_HOUR_OF_DAY, 1); // принудительный перерасчёт времени
var_dump($cal->inDaylightTime()); // true
```
