---
navigation:
  - intlcalendar.getlocale.md: '« IntlCalendar::getLocale'
  - intlcalendar.getminimaldaysinfirstweek.md: 'IntlCalendar::getMinimalDaysInFirstWeek »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
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

Отримує глобальне максимальне значення поля у цьому конкретному календарі. Це значення більше або дорівнює значенню, що повертається [IntlCalendar::getActualMaximum()](intlcalendar.getactualmaximum.md), яке, у свою чергу, більше або дорівнює значенню, що повертається [IntlCalendar::getLeastMaximum()](intlcalendar.getleastmaximum.md)

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.md) [констант](class.intlcalendar.md#intlcalendar.constants) полів типу дата/час. Ціла кількість від `0` до **`IntlCalendar::FIELD_COUNT`**

### Значення, що повертаються

Ціле число (int), що представляє значення для даного поля або **`false`** у разі виникнення помилки.

### Дивіться також

-   [IntlCalendar::getActualMaximum()](intlcalendar.getactualmaximum.md) - Максимальне значення для поля з урахуванням поточного часу об'єкта
-   [IntlCalendar::getLeastMaximum()](intlcalendar.getleastmaximum.md) - Отримує найменший локальний максимум для поля
-   [IntlCalendar::getMinimum()](intlcalendar.getminimum.md) - Отримує глобальне мінімальне значення поля
