---
navigation:
  - intlcalendar.set.md: '« IntlCalendar::set'
  - intlcalendar.setdatetime.md: 'IntlCalendar::setDateTime »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::setDate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::setDate

(PHP 8 >= 8.3.0)

IntlCalendar::setDate — Встановлює поля дати

### Опис

```methodsynopsis
public IntlCalendar::setDate(int $year, int $month, int $dayOfMonth): void
```

Встановлює в поля дати задане значення.

### Список параметрів

`year`

Новое значение для\*\*`IntlCalendar::FIELD_YEAR`\*\*

`month`

Новое значение для\*\*`IntlCalendar::FIELD_MONTH`\*\*. Послідовність місяців починається з нуля, тобто січень позначається як 0, лютий – 1, …, грудень – 11, а грудень (якщо він є у календарі) – 12.

`dayOfMonth`

Новое значение для\*\*`IntlCalendar::FIELD_DAY_OF_MONTH`\*\*

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад использования метода**IntlCalendar::setDate()\*\*\*\*

```php
<?php
$intlCal = IntlCalendar::createInstance('UTC');

$intlCal->setDate(2012, 1, 29);
?>
```
