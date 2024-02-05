---
navigation:
  - intlcalendar.setlenient.md: '« IntlCalendar::setLenient'
  - intlcalendar.setrepeatedwalltimeoption.md: 'IntlCalendar::setRepeatedWallTimeOption »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::setMinimalDaysInFirstWeek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::setMinimalDaysInFirstWeek

(PHP 5 >= 5.5.1, PHP 7, PHP 8)

IntlCalendar::setMinimalDaysInFirstWeek — Встановлює мінімальну кількість днів, яка може бути в першому тижні на рік або місяць

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::setMinimalDaysInFirstWeek(int $days): true
```

Процедурний стиль

```methodsynopsis
intlcal_set_minimal_days_in_first_week(IntlCalendar $calendar, int $days): true
```

Встановлює найменшу кількість днів, які мають пройти у перший тиждень року чи місяця у новому році чи місяці. Наприклад, у григоріанському календарі, якщо це значення дорівнює 1, то перший тиждень року обов'язково включатиме 1 січня, а якщо це значення дорівнює 7, то тиждень з 1 січня буде першим тижнем року, тільки якщо день тижня 1 січня збігається з днем ​​тижня, повертається [IntlCalendar::getFirstDayOfWeek()](intlcalendar.getfirstdayofweek.md); інакше це буде останній тиждень минулого року.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`days`

Кількість мінімальних днів, які необхідно встановити.

### Значення, що повертаються

Функція завжди повертає **`true`**

### Помилки

Метод викидає помилку [ValueError](class.valueerror.md), якщо параметр `days`находится вне диапазона (меньше или больше`7`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі некоректного введення даних тепер видається помилка [ValueError](class.valueerror.md); раніше поверталося значення **`false`** |
