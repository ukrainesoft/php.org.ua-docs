---
navigation:
  - intlcalendar.getnow.md: '« IntlCalendar::getNow'
  - intlcalendar.getskippedwalltimeoption.md: 'IntlCalendar::getSkippedWallTimeOption »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getRepeatedWallTimeOption'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::getRepeatedWallTimeOption

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getRepeatedWallTimeOption — Отримує поведінку для обробки часу процесора, що повторюється.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getRepeatedWallTimeOption(): int
```

Процедурний стиль

```methodsynopsis
intlcal_get_repeated_wall_time_option(IntlCalendar $calendar): int
```

Отримує поточну стратегію роботи з часом процесора, яка повторюється щоразу, коли годинник переводиться назад під час переходів на літній час. Значення за замовчуванням - **`IntlCalendar::WALLTIME_LAST`**

Для цієї функції потрібний ICU 4.9 або новіший.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

### Значення, що повертаються

Одна из констант:**`IntlCalendar::WALLTIME_FIRST`**или**`IntlCalendar::WALLTIME_LAST`**

### Приклади

**Пример #1 Пример использования**IntlCalendar::getRepeatedWallTimeOption()\*\*\*\*

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'en_US');
ini_set('intl.error_level', E_WARNING);

// 27 октября в 02:00 часы переводятся на 1 час назад с GMT+01 на GMT+00.
$cal = new IntlGregorianCalendar(2013, 9 /* Октябрь */, 27, 1, 30);

var_dump($cal->getRepeatedWalltimeOption()); // 0 WALLTIME_LAST

$formatter = IntlDateFormatter::create(
    NULL,
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'UTC'
);
var_dump($formatter->format($cal->getTime() / 1000.));

$cal->setRepeatedWalltimeOption(IntlCalendar::WALLTIME_FIRST);
var_dump($cal->getRepeatedWalltimeOption()); // 1 WALLTIME_FIRST
$cal->set(IntlCalendar::FIELD_HOUR_OF_DAY, 1);

var_dump($formatter->format($cal->getTime() / 1000.));
```

Результат виконання наведеного прикладу:

```
int(0)
string(42) "Sunday, October 27, 2013 at 1:30:00 AM GMT"
int(1)
string(43) "Sunday, October 27, 2013 at 12:30:00 AM GMT"
```

### Дивіться також

-   [IntlCalendar::getSkippedWallTimeOption()](intlcalendar.getskippedwalltimeoption.md) \- отримує поведінку для обробки пропущеного часу процесора
-   [IntlCalendar::setSkippedWallTimeOption()](intlcalendar.setskippedwalltimeoption.md) \- Встановлює поведінку для обробки пропущеного часу процесора при позитивних переходах усунення часового поясу
-   [IntlCalendar::setRepeatedWallTimeOption()](intlcalendar.setrepeatedwalltimeoption.md) \- Встановлює поведінку для обробки часу процесора, що повторюється, при негативних переходах зміщення часового поясу
