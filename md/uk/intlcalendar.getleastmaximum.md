---
navigation:
  - intlcalendar.getkeywordvaluesforlocale.md: '« IntlCalendar::getKeywordValuesForLocale'
  - intlcalendar.getlocale.md: 'IntlCalendar::getLocale »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getLeastMaximum'
---
# IntlCalendar::getLeastMaximum

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getLeastMaximum — Отримує найменший локальний максимум для поля

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getLeastMaximum(int $field): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_least_maximum(IntlCalendar $calendar, int $field): int|false
```

Повертає найменший локальний максимум для поля. Це має бути значення, менше або рівне значенню, що повертається **IntlCalendar::getActualMaxmimum()**, яке, у свою чергу, менше або дорівнює значенню, що повертається [IntlCalendar::getMaximum()](intlcalendar.getmaximum.md)

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.md) [констант](class.intlcalendar.md#intlcalendar.constants) полів типу дата/час. Ціла кількість від `0` до **`IntlCalendar::FIELD_COUNT`**

### Значення, що повертаються

Ціле число (int), що представляє значення поля або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад максимального значення**

```php
<?php
ini_set('date.timezone', 'UTC');
ini_set('intl.default_locale', 'it_IT');

$cal = new IntlGregorianCalendar(2013, 3 /* April */, 6);
var_dump(
    $cal->getLeastMaximum(IntlCalendar::FIELD_DAY_OF_MONTH),  // 28
    $cal->getActualMaximum(IntlCalendar::FIELD_DAY_OF_MONTH), // 30
    $cal->getMaximum(IntlCalendar::FIELD_DAY_OF_MONTH)        // 31
);
```

Результат виконання цього прикладу:

```
int(28)
int(30)
int(31)
```

### Дивіться також

-   [IntlCalendar::getActualMaximum()](intlcalendar.getactualmaximum.md) - Максимальне значення для поля з урахуванням поточного часу об'єкта
-   [IntlCalendar::getMaximum()](intlcalendar.getmaximum.md) - Отримує глобальне максимальне значення поля
-   [IntlCalendar::getGreatestMinimum()](intlcalendar.getgreatestminimum.md) - Отримує найбільше локальне мінімальне значення поля
