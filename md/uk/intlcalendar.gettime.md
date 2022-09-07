---
navigation:
  - intlcalendar.getskippedwalltimeoption.md: '« IntlCalendar::getSkippedWallTimeOption'
  - intlcalendar.gettimezone.md: 'IntlCalendar::getTimeZone »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getTime'
---
# IntlCalendar::getTime

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getTime — Отримує час, представлений на даний момент об'єктом

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getTime(): float|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_time(IntlCalendar $calendar): float|false
```

Повертає час, пов'язаний із цим об'єктом, виражений у мілісекундах з початку епохи Unix.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

### Значення, що повертаються

Число з плаваючою точкою (float), що представляє кількість мілісекунд, що пройшли з початку епохи Unix (1 січня 1970 00:00:00 UTC) або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::getTime()****

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'en_US');

$cal = new IntlGregorianCalendar(2013, 4 /* Май */, 1, 0, 0, 0);
$time = $cal->getTime();
var_dump($time, $time / 1000 == strtotime('2013-05-01 00:00:00')); //true
```

Результат виконання цього прикладу:

```
float(1367362800000)
bool(true)
```

### Дивіться також

-   [IntlCalendar::getNow()](intlcalendar.getnow.md) - Отримує число, що становить поточний час
