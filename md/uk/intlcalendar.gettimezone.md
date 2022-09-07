---
navigation:
  - intlcalendar.gettime.md: '« IntlCalendar::getTime'
  - intlcalendar.gettype.md: 'IntlCalendar::getType »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getTimeZone'
---
# IntlCalendar::getTimeZone

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getTimeZone — Отримує часовий пояс об'єкта

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getTimeZone(): IntlTimeZone|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_time_zone(IntlCalendar $calendar): IntlTimeZone|false
```

Повертає об'єкт [IntlTimeZone](class.intltimezone.md), пов'язані з календарем.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

### Значення, що повертаються

Об'єкт [IntlTimeZone](class.intltimezone.md), що відповідає тому, що використовується всередині об'єкта. Повертає **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::getTimeZone()****

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'en_US');

$cal = IntlCalendar::createInstance();
print_r($cal->getTimeZone());

$cal->setTimeZone('UTC');
print_r($cal->getTimeZone());

$cal = IntlCalendar::fromDateTime('2012-01-01 00:00:00 GMT+03:33');
print_r($cal->getTimeZone());
```

Результат виконання цього прикладу:

```
IntlTimeZone Object
(
    [valid] => 1
    [id] => Europe/Lisbon
    [rawOffset] => 0
    [currentOffset] => 3600000
)
IntlTimeZone Object
(
    [valid] => 1
    [id] => UTC
    [rawOffset] => 0
    [currentOffset] => 0
)
IntlTimeZone Object
(
    [valid] => 1
    [id] => GMT+03:33
    [rawOffset] => 12780000
    [currentOffset] => 12780000
)
```

### Дивіться також

-   [IntlCalendar::setTimeZone()](intlcalendar.settimezone.md) - Встановлює часовий пояс, що використовується календарем
-   [IntlCalendar::createInstance()](intlcalendar.createinstance.md) - Створює новий об'єкт IntlCalendar
-   [IntlGregorianCalendar::construct()](intlgregoriancalendar.construct.md) - Конструктор класу григоріанського календаря
