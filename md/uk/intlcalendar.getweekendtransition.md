---
navigation:
  - intlcalendar.gettype.html: '« IntlCalendar::getType'
  - intlcalendar.indaylighttime.html: 'IntlCalendar::inDaylightTime »'
  - index.html: PHP Manual
  - class.intlcalendar.html: IntlCalendar
title: 'IntlCalendar::getWeekendTransition'
---
# IntlCalendar::getWeekendTransition

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getWeekendTransition — Отримує час, коли вихідні починаються або закінчуються.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getWeekendTransition(int $dayOfWeek): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_weekend_transition(IntlCalendar $calendar, int $dayOfWeek): int|false
```

Повертає кількість мілісекундів після опівночі, коли вихідні починаються або закінчуються.

Застосовується тільки для днів тижня, для яких [IntlCalendar::getDayOfWeekType()](intlcalendar.getdayofweektype.html) повертає або **`IntlCalendar::DOW_TYPE_WEEKEND_OFFSET`**, або **`IntlCalendar::DOW_TYPE_WEEKEND_CEASE`**. Виклик цієї функції для інших днів тижня є помилкою.

Для цієї функції потрібний ICU 4.4 або новіший.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`dayOfWeek`

Одна з констант: **`IntlCalendar::DOW_SUNDAY`** **`IntlCalendar::DOW_MONDAY`** **`IntlCalendar::DOW_SATURDAY`**

### Значення, що повертаються

Кількість мілісекунд після опівночі, коли вихідні починаються або закінчуються або **`false`** у разі виникнення помилки.

### Приклади

Приклади дивіться в описі функції [IntlCalendar::getDayOfWeekType()](intlcalendar.getdayofweektype.html)
