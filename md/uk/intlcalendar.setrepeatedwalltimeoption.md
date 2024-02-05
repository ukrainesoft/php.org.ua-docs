---
navigation:
  - intlcalendar.setminimaldaysinfirstweek.md: '« IntlCalendar::setMinimalDaysInFirstWeek'
  - intlcalendar.setskippedwalltimeoption.md: 'IntlCalendar::setSkippedWallTimeOption »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::setRepeatedWallTimeOption'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::setRepeatedWallTimeOption

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::setRepeatedWallTimeOption — Встановлює поведінку для обробки часу процесора, що повторюється, при негативних переходах зміщення часового поясу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::setRepeatedWallTimeOption(int $option): true
```

Процедурний стиль

```methodsynopsis
intlcal_set_repeated_wall_time_option(IntlCalendar $calendar, int $option): true
```

Встановлює поточну стратегію роботи з часом процесора, яка повторюється щоразу, коли годинник переводиться назад під час переходу на літній час. Значення за замовчуванням - **`IntlCalendar::WALLTIME_LAST`**(момент после перехода на летнее время). Другое возможное значение -**`IntlCalendar::WALLTIME_FIRST`** (Момент, який настає під час переходу на літню пору).

Для цієї функції потрібний ICU 4.9 або новіший.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`option`

Одна из констант:**`IntlCalendar::WALLTIME_FIRST`** або **`IntlCalendar::WALLTIME_LAST`**

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |

### Приклади

Дивіться приклади у описі функції [IntlCalendar::getRepeatedWallTimeOption()](intlcalendar.getrepeatedwalltimeoption.md)

### Дивіться також

-   [intlCalendar::getRepeatedWallTimeOption()](intlcalendar.getrepeatedwalltimeoption.md) \- Отримує поведінку для обробки повторюваного часу процесора
-   [intlCalendar::setSkippedWallTimeOption()](intlcalendar.setskippedwalltimeoption.md) \- Встановлює поведінку для обробки пропущеного часу процесора при позитивних переходах усунення часового поясу
-   [intlCalendar::getSkippedWallTimeOption()](intlcalendar.getskippedwalltimeoption.md) \- отримує поведінку для обробки пропущеного часу процесора
