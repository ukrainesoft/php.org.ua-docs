---
navigation:
  - intlcalendar.getminimaldaysinfirstweek.md: '« IntlCalendar::getMinimalDaysInFirstWeek'
  - intlcalendar.getnow.md: 'IntlCalendar::getNow »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getMinimum'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Отримує глобальне мінімальне значення поля у цьому конкретному календарі. Це значення менше або дорівнює значенню, що повертається [IntlCalendar::getActualMinimum()](intlcalendar.getactualminimum.md), яке, у свою чергу, менше або дорівнює значенню, що повертається [IntlCalendar::getGreatestMinimum()](intlcalendar.getgreatestminimum.md). Для григоріанського календаря ці три функції завжди повертають те саме значення (для кожного поля).

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.md) [констант](class.intlcalendar.md#intlcalendar.constants)полей типа дата/время. Целое число от до\*\*`IntlCalendar::FIELD_COUNT`\*\*

### Значення, що повертаються

Целое число (int), представляющее значение для данного поля или\*\*`false`\*\*в случае возникновения ошибки.
