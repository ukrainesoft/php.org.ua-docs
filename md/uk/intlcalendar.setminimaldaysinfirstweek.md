---
navigation:
  - intlcalendar.setlenient.html: '« IntlCalendar::setLenient'
  - intlcalendar.setrepeatedwalltimeoption.html: 'IntlCalendar::setRepeatedWallTimeOption »'
  - index.html: PHP Manual
  - class.intlcalendar.html: IntlCalendar
title: 'IntlCalendar::setMinimalDaysInFirstWeek'
---
# IntlCalendar::setMinimalDaysInFirstWeek

(PHP 5> = 5.5.1, PHP 7, PHP 8)

IntlCalendar::setMinimalDaysInFirstWeek — Встановлює мінімальну кількість днів, яка може бути в першому тижні на рік або місяць

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::setMinimalDaysInFirstWeek(int $days): bool
```

Процедурний стиль

```methodsynopsis
intlcal_set_minimal_days_in_first_week(IntlCalendar $calendar, int $days): bool
```

Встановлює найменшу кількість днів, які мають пройти у перший тиждень року чи місяця у новому році чи місяці. Наприклад, у григоріанському календарі, якщо це значення дорівнює 1, то перший тиждень року обов'язково включатиме 1 січня, а якщо це значення дорівнює 7, то тиждень з 1 січня буде першим тижнем року, тільки якщо день тижня 1 січня збігається з днем ​​тижня, повертається [IntlCalendar::getFirstDayOfWeek()](intlcalendar.getfirstdayofweek.html); інакше це буде останній тиждень минулого року.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`days`

Кількість мінімальних днів, які необхідно встановити.

### Значення, що повертаються

**`true`** у разі успішного виконання, **`false`** у разі виникнення помилки.
