---
navigation:
  - intldateformatter.getcalendarobject.md: '« IntlDateFormatter::getCalendarObject'
  - intldateformatter.islenient.md: 'IntlDateFormatter::isLenient »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::getTimeZone'
---
# IntlDateFormatter::getTimeZone

# datefmtgettimezone

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL intl >= 3.0.0)

IntlDateFormatter::getTimeZone -- datefmtgettimezone — Отримує часовий пояс засобу форматування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getTimeZone(): IntlTimeZone|false
```

Процедурний стиль

```methodsynopsis
datefmt_get_timezone(IntlDateFormatter $formatter): IntlTimeZone|false
```

Повертає об'єкт [IntlTimeZone](class.intltimezone.md), що представляє часовий пояс, який використовуватиметься цим об'єктом для форматування дати та часу. При форматуванні об'єктів [IntlCalendar](class.intlcalendar.md) і [DateTime](class.datetime.md) За допомогою цього [IntlDateFormatter](class.intldateformatter.md), використовуваний часовий пояс буде той, який повертається цим методом, а не той, який пов'язаний з об'єктами, що форматуються.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Пов'язаний об'єкт [IntlTimeZone](class.intltimezone.md) або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlDateFormatter::getTimeZone()****

```php
<?php

$madrid = IntlDateFormatter::create(NULL, NULL, NULL, 'Europe/Madrid');
$lisbon = IntlDateFormatter::create(NULL, NULL, NULL, 'Europe/Lisbon');

var_dump($madrid->getTimezone());
echo $madrid->getTimezone()->getDisplayName(
        false, IntlTimeZone::DISPLAY_GENERIC_LOCATION, "en_US"), "\n";
echo $lisbon->getTimeZone()->getId(), "\n";
//Идентификатор также можно получить с помощью ->getTimezoneId()
echo $lisbon->getTimeZoneId(), "\n";
```

Результат виконання цього прикладу:

```
object(IntlTimeZone)#4 (4) {
  ["valid"]=>
  bool(true)
  ["id"]=>
  string(13) "Europe/Madrid"
  ["rawOffset"]=>
  int(3600000)
  ["currentOffset"]=>
  int(7200000)
}
Spain Time
Europe/Lisbon
Europe/Lisbon
```

### Дивіться також

-   [IntlDateFormatter::getTimeZoneId()](intldateformatter.gettimezoneid.md) - Отримує ідентифікатор часового поясу, який використовується IntlDateFormatter
-   [IntlDateFormatter::setTimeZone()](intldateformatter.settimezone.md) - Встановлює часовий пояс засобу форматування
-   [IntlTimeZone](class.intltimezone.md)
