Встановлює поведінку для обробки часу процесора, що повторюється, при негативних переходах зміщення часового поясу

-   [« IntlCalendar::setMinimalDaysInFirstWeek](intlcalendar.setminimaldaysinfirstweek.html)
    
-   [IntlCalendar::setSkippedWallTimeOption »](intlcalendar.setskippedwalltimeoption.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Встановлює поведінку для обробки часу процесора, що повторюється, при негативних переходах зміщення часового поясу
    

# IntlCalendar::setRepeatedWallTimeOption

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::setRepeatedWallTimeOption — Встановлює поведінку для обробки часу процесора, що повторюється, при негативних переходах зміщення часового поясу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::setRepeatedWallTimeOption(int $option): bool
```

Процедурний стиль

```methodsynopsis
intlcal_set_repeated_wall_time_option(IntlCalendar $calendar, int $option): bool
```

Встановлює поточну стратегію роботи з часом процесора, яка повторюється щоразу, коли годинник переводиться назад під час переходу на літній час. Значення за замовчуванням - **`IntlCalendar::WALLTIME_LAST`** (Момент після переходу на літню пору). Інше можливе значення - **`IntlCalendar::WALLTIME_FIRST`** (Момент, який настає під час переходу на літню пору).

Для цієї функції потрібний ICU 4.9 або новіший.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`option`

Одна з констант: **`IntlCalendar::WALLTIME_FIRST`** або **`IntlCalendar::WALLTIME_LAST`**

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

Дивіться приклади у описі функції [IntlCalendar::getRepeatedWallTimeOption()](intlcalendar.getrepeatedwalltimeoption.html)

### Дивіться також

-   [intlCalendar::getRepeatedWallTimeOption()](intlcalendar.getrepeatedwalltimeoption.html) - Отримує поведінку для обробки повторюваного часу процесора
-   [intlCalendar::setSkippedWallTimeOption()](intlcalendar.setskippedwalltimeoption.html) - Встановлює поведінку для обробки пропущеного часу процесора при позитивних переходах усунення часового поясу
-   [intlCalendar::getSkippedWallTimeOption()](intlcalendar.getskippedwalltimeoption.html) - отримує поведінку для обробки пропущеного часу процесора