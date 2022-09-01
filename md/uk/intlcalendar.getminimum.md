---
navigation:
  - intlcalendar.getminimaldaysinfirstweek.html: '« IntlCalendar::getMinimalDaysInFirstWeek'
  - intlcalendar.getnow.html: 'IntlCalendar::getNow »'
  - index.html: PHP Manual
  - class.intlcalendar.html: IntlCalendar
title: 'IntlCalendar::getMinimum'
---
# IntlCalendar::getMinimum

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getMinimum — Отримує глобальне мінімальне значення поля

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getMinimum(int $field): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_minimum(IntlCalendar $calendar, int $field): int|false
```

Отримує глобальне мінімальне значення поля у цьому конкретному календарі. Це значення менше або дорівнює значенню, що повертається [IntlCalendar::getActualMinimum()](intlcalendar.getactualminimum.html), яке, у свою чергу, менше або дорівнює значенню, що повертається [IntlCalendar::getGreatestMinimum()](intlcalendar.getgreatestminimum.html). Для григоріанського календаря ці три функції завжди повертають те саме значення (для кожного поля).

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.html) [констант](class.intlcalendar.html#intlcalendar.constants) полів типу дата/час. Ціла кількість від `0` до **`IntlCalendar::FIELD_COUNT`**

### Значення, що повертаються

Ціле число (int), що представляє значення для даного поля або **`false`** у разі виникнення помилки.
