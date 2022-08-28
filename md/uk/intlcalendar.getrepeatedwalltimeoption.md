Отримує поведінку для обробки повторюваного часу процесора

-   [« IntlCalendar::getNow](intlcalendar.getnow.html)
    
-   [IntlCalendar::getSkippedWallTimeOption »](intlcalendar.getskippedwalltimeoption.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Отримує поведінку для обробки повторюваного часу процесора
    

# IntlCalendar::getRepeatedWallTimeOption

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getRepeatedWallTimeOption — Отримує поведінку для обробки повторюваного часу процесора

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

Екземпляр [IntlCalendar](class.intlcalendar.html)

### Значення, що повертаються

Одна з констант: **`IntlCalendar::WALLTIME_FIRST`** або **`IntlCalendar::WALLTIME_LAST`**

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::getRepeatedWallTimeOption()****

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'en_US');
ini_set('intl.error_level', E_WARNING);

// 27 октября в 02:00 часы переводятся на 1 час назад с GMT+01 на GMT+00.
$cal = new IntlGregorianCalendar(2013, 9 /* Октябрь */, 27, 1, 30);

var_dump($cal->getRepeatedWalltimeOption()); // 0 WALLTIME_LAST

$formatter = IntlDateFormatter::create(
    NULL,
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'UTC'
);
var_dump($formatter->format($cal->getTime() / 1000.));

$cal->setRepeatedWalltimeOption(IntlCalendar::WALLTIME_FIRST);
var_dump($cal->getRepeatedWalltimeOption()); // 1 WALLTIME_FIRST
$cal->set(IntlCalendar::FIELD_HOUR_OF_DAY, 1);

var_dump($formatter->format($cal->getTime() / 1000.));
```

Результат виконання цього прикладу:

```
int(0)
string(42) "Sunday, October 27, 2013 at 1:30:00 AM GMT"
int(1)
string(43) "Sunday, October 27, 2013 at 12:30:00 AM GMT"
```

### Дивіться також

-   [IntlCalendar::getSkippedWallTimeOption()](intlcalendar.getskippedwalltimeoption.html) - отримує поведінку для обробки пропущеного часу процесора
-   [IntlCalendar::setSkippedWallTimeOption()](intlcalendar.setskippedwalltimeoption.html) - Встановлює поведінку для обробки пропущеного часу процесора при позитивних переходах усунення часового поясу
-   [IntlCalendar::setRepeatedWallTimeOption()](intlcalendar.setrepeatedwalltimeoption.html) - Встановлює поведінку для обробки часу процесора, що повторюється, при негативних переходах зміщення часового поясу