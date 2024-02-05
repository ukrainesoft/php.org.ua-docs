---
navigation:
  - intldateformatter.gettimezoneid.md: '« IntlDateFormatter::getTimeZoneId'
  - intldateformatter.gettimezone.md: 'IntlDateFormatter::getTimeZone »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::getCalendarObject'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlDateFormatter::getCalendarObject

# datefmt\_get\_calendar\_object

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL intl >= 3.0.0)

IntlDateFormatter::getCalendarObject -- datefmt\_get\_calendar\_object — Отримує копію об'єкта календаря засобу форматування.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getCalendarObject(): IntlCalendar|false|null
```

Процедурний стиль

```methodsynopsis
datefmt_get_calendar_object(IntlDateFormatter $formatter): IntlCalendar|false|null
```

Отримує копію об'єкта календаря, який використовується для внутрішніх цілей засобом форматування. Календар матиме тип (наприклад, грегоріанський, японський, буддійський, рок, перський, ісламський тощо) та часовий пояс, які відповідають типу та часовому поясу, що використовуються засобом форматування. Дата та час об'єкта не вказані.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Копія внутрішнього об'єкта календаря, що використовується засобом форматування або \*\*`null`\*\*якщо нічого не було встановлено або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** IntlDateFormatter::getCalendarObject()\*\*\*\*

```php
<?php
$formatter = IntlDateFormatter::create(
    "fr_FR@calendar=islamic",
    NULL,
    NULL,
    "GMT-01:00",
    IntlDateFormatter::TRADITIONAL
);

$cal = $formatter->getCalendarObject();

var_dump(
    $cal->getType(),
    $cal->getTimeZone(),
    $cal->getLocale(Locale::VALID_LOCALE)
);
```

Результат виконання наведеного прикладу:

```
string(7) "islamic"
object(IntlTimeZone)#3 (4) {
  ["valid"]=>
  bool(true)
  ["id"]=>
  string(9) "GMT-01:00"
  ["rawOffset"]=>
  int(-3600000)
  ["currentOffset"]=>
  int(-3600000)
}
string(5) "fr_FR"
```

### Дивіться також

-   [IntlDateFormatter::getCalendar()](intldateformatter.getcalendar.md) \- Отримує тип календаря для об'єкта IntlDateFormatter
-   [IntlDateFormatter::setCalendar()](intldateformatter.setcalendar.md) \- Встановлює тип календаря, який використовується засобом форматування
-   [IntlCalendar](class.intlcalendar.md)
