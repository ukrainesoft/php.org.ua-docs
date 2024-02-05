---
navigation:
  - intlcalendar.setdate.md: '« IntlCalendar::setDate'
  - intlcalendar.setfirstdayofweek.md: 'IntlCalendar::setFirstDayOfWeek »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::setDateTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::setDateTime

(PHP 8 >= 8.3.0)

IntlCalendar::setDateTime — Встановлює поля дати та часу

### Опис

```methodsynopsis
public IntlCalendar::setDateTime(    int $year,    int $month,    int $dayOfMonth,    int $hour,    int $minute,    int $second = null): void
```

Встановлює в поля дати та часу задане значення.

### Список параметрів

`year`

Новое значение для\*\*`IntlCalendar::FIELD_YEAR`\*\*

`month`

Новое значение для\*\*`IntlCalendar::FIELD_MONTH`\*\*. Послідовність місяців починається з нуля, тобто січень позначається як 0, лютий – 1, …, грудень – 11, а грудень (якщо він є у календарі) – 12.

`dayOfMonth`

Новое значение для\*\*`IntlCalendar::FIELD_DAY_OF_MONTH`\*\*

`hour`

Новое значение для\*\*`IntlCalendar::FIELD_HOUR_OF_DAY`\*\*

`minute`

Новое значение для\*\*`IntlCalendar::FIELD_MINUTE`\*\*

`second`

Новое значение для\*\*`IntlCalendar::FIELD_SECOND`\*\*

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад использования метода**IntlCalendar::setDateTime()\*\*\*\*

```php
<?php
$intlCal = IntlCalendar::createInstance('UTC');

$intlCal->setDateTime(2012, 1, 29, 23, 58);
?>
```
