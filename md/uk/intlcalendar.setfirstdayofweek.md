---
navigation:
  - intlcalendar.setdatetime.md: '« IntlCalendar::setDateTime'
  - intlcalendar.setlenient.md: 'IntlCalendar::setLenient »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::setFirstDayOfWeek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::setFirstDayOfWeek

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::setFirstDayOfWeek — Встановлює день, який є початком тижня

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::setFirstDayOfWeek(int $dayOfWeek): true
```

Процедурний стиль

```methodsynopsis
intlcal_set_first_day_of_week(IntlCalendar $calendar, int $dayOfWeek): true
```

Визначає день тижня, що вважається початком тижня. Це впливає на поведінку полів, які залежать від концепції початку та кінця тижня, наприклад: **`IntlCalendar::FIELD_WEEK_OF_YEAR`** і **`IntlCalendar::FIELD_YEAR_WOY`**

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`dayOfWeek`

Одна из констант\*\*`IntlCalendar::DOW_SUNDAY`\*\* **`IntlCalendar::DOW_MONDAY`** **`IntlCalendar::DOW_SATURDAY`**

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |

### Приклади

**Приклад #1 Приклад використання** IntlCalendar::setFirstDayOfWeek()\*\*\*\*

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'es_ES');

$cal = IntlCalendar::createInstance();
$cal->set(2013, 5 /* Июнь */, 30); // Воскресенье

var_dump($cal->getFirstDayOfWeek()); // 2 (Понедельник)

echo IntlDateFormatter::formatObject($cal, <<<EOD
'местный день недели: 'cc'
неделя месяца    : 'W'
неделя года     : 'ww
EOD
), "\n";

$cal->setFirstDayOfWeek(IntlCalendar::DOW_SUNDAY);

echo IntlDateFormatter::formatObject($cal, <<<EOD
'местный день недели: 'cc'
неделя месяца    : 'W'
неделя года     : 'ww
EOD
), "\n";
```

Результат виконання наведеного прикладу:

```
int(2)
местный день недели: 7
неделя месяца    : 4
неделя года     : 26
местный день недели: 1
неделя месяца    : 5
неделя года     : 27
```
