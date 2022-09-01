---
navigation:
  - intlcalendar.getrepeatedwalltimeoption.html: '« IntlCalendar::getRepeatedWallTimeOption'
  - intlcalendar.gettime.html: 'IntlCalendar::getTime »'
  - index.html: PHP Manual
  - class.intlcalendar.html: IntlCalendar
title: 'IntlCalendar::getSkippedWallTimeOption'
---
# IntlCalendar::getSkippedWallTimeOption

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getSkippedWallTimeOption — Отримує поведінку для обробки пропущеного часу процесора

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getSkippedWallTimeOption(): int
```

Процедурний стиль

```methodsynopsis
intlcal_get_skipped_wall_time_option(IntlCalendar $calendar): int
```

Отримує поточну стратегію для роботи з часом процесора, що пропускається щоразу, коли годинник переводиться під час переходів часу на літній час. Значення за замовчуванням - **`IntlCalendar::WALLTIME_LAST`**

Щоб ця опція мала якийсь ефект, календар має бути в [м'якому](intlcalendar.setlenient.html) режимі, в іншому випадку спроба встановити неіснуючий час викликає помилку.

Для цієї функції потрібний ICU 4.9 або новіший.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

### Значення, що повертаються

Одна з констант: **`IntlCalendar::WALLTIME_FIRST`** **`IntlCalendar::WALLTIME_LAST`** або **`IntlCalendar::WALLTIME_NEXT_VALID`**

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::getSkippedWallTimeOption()****

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'en_US');
ini_set('intl.error_level', E_WARNING);

// 31 марта в 01:00 часы переводятся на 1 час вперёд и с GMT+00 на GMT+01.
$cal = new IntlGregorianCalendar(2013, 2 /* March */, 31, 1, 30);

var_dump(
    $cal->isLenient(),               // true
    $cal->getSkippedWalltimeOption() // 0 WALLTIME_LAST
);

$formatter = IntlDateFormatter::create(
    NULL,
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'UTC'
);
var_dump($formatter->format($cal->getTime() / 1000));

$cal->setSkippedWallTimeOption(IntlCalendar::WALLTIME_FIRST);
var_dump($cal->getSkippedWalltimeOption()); // 1 WALLTIME_FIRST
$cal->set(IntlCalendar::FIELD_HOUR_OF_DAY, 1);

var_dump($formatter->format($cal->getTime() / 1000));

$cal->setSkippedWallTimeOption(IntlCalendar::WALLTIME_NEXT_VALID);
var_dump($cal->getSkippedWalltimeOption()); // 2 WALLTIME_NEXT_VALID
$cal->set(IntlCalendar::FIELD_HOUR_OF_DAY, 1);

var_dump($formatter->format($cal->getTime() / 1000));
```

Результат виконання цього прикладу:

```
bool(true)
int(0)
string(40) "Sunday, March 31, 2013 at 1:30:00 AM GMT"
int(1)
string(41) "Sunday, March 31, 2013 at 12:30:00 AM GMT"
int(2)
string(40) "Sunday, March 31, 2013 at 1:00:00 AM GMT"
```

### Дивіться також

-   [IntlCalendar::getRepeatedWallTimeOption()](intlcalendar.getrepeatedwalltimeoption.html) - Отримує поведінку для обробки повторюваного часу процесора
-   [IntlCalendar::setSkippedWallTimeOption()](intlcalendar.setskippedwalltimeoption.html) - Встановлює поведінку для обробки пропущеного часу процесора при позитивних переходах усунення часового поясу
-   [IntlCalendar::setRepeatedWallTimeOption()](intlcalendar.setrepeatedwalltimeoption.html) - Встановлює поведінку для обробки часу процесора, що повторюється, при негативних переходах зміщення часового поясу
