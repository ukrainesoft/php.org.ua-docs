---
navigation:
  - intlcalendar.getfirstdayofweek.md: '« IntlCalendar::getFirstDayOfWeek'
  - intlcalendar.getkeywordvaluesforlocale.md: 'IntlCalendar::getKeywordValuesForLocale »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getGreatestMinimum'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::getGreatestMinimum

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getGreatestMinimum — Отримує найбільше локальне мінімальне значення поля

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getGreatestMinimum(int $field): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_greatest_minimum(IntlCalendar $calendar, int $field): int|false
```

Повертає найбільше локальне мінімальне значення поля. Це має бути значення, більше або рівне значенню, що повертається [IntlCalendar::getActualMinimum()](intlcalendar.getactualminimum.md), яке, у свою чергу, більше або дорівнює значенню, що повертається [IntlCalendar::getMinimum()](intlcalendar.getminimum.md). Всі ці три функції повертають те саме значення для григоріанського календаря.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.md) [констант](class.intlcalendar.md#intlcalendar.constants)полей типа дата/время. Целое число от до\*\*`IntlCalendar::FIELD_COUNT`\*\*

### Значення, що повертаються

Целое число (int), представляющее значение поля или\*\*`false`\*\*в случае возникновения ошибки.
