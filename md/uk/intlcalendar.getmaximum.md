---
navigation:
  - intlcalendar.getlocale.html: '« IntlCalendar::getLocale'
  - intlcalendar.getminimaldaysinfirstweek.html: 'IntlCalendar::getMinimalDaysInFirstWeek »'
  - index.html: PHP Manual
  - class.intlcalendar.html: IntlCalendar
title: 'IntlCalendar::getMaximum'
---
# IntlCalendar::getMaximum

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getMaximum — Отримує глобальне максимальне значення поля

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getMaximum(int $field): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_maximum(IntlCalendar $calendar, int $field): int|false
```

Отримує глобальне максимальне значення поля у цьому конкретному календарі. Це значення більше або дорівнює значенню, що повертається [IntlCalendar::getActualMaximum()](intlcalendar.getactualmaximum.html), яке, у свою чергу, більше або дорівнює значенню, що повертається [IntlCalendar::getLeastMaximum()](intlcalendar.getleastmaximum.html)

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.html) [констант](class.intlcalendar.html#intlcalendar.constants) полів типу дата/час. Ціла кількість від `0` до **`IntlCalendar::FIELD_COUNT`**

### Значення, що повертаються

Ціле число (int), що представляє значення для даного поля або **`false`** у разі виникнення помилки.

### Дивіться також

-   [IntlCalendar::getActualMaximum()](intlcalendar.getactualmaximum.html) - Максимальне значення для поля з урахуванням поточного часу об'єкта
-   [IntlCalendar::getLeastMaximum()](intlcalendar.getleastmaximum.html) - Отримує найменший локальний максимум для поля
-   [IntlCalendar::getMinimum()](intlcalendar.getminimum.html) - Отримує глобальне мінімальне значення поля
