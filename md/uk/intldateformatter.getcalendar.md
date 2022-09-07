---
navigation:
  - intldateformatter.formatobject.md: '« IntlDateFormatter::formatObject'
  - intldateformatter.getdatetype.md: 'IntlDateFormatter::getDateType »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::getCalendar'
---
# IntlDateFormatter::getCalendar

# datefmtgetcalendar

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getCalendar -- datefmtgetcalendar — Отримує тип календаря, який використовується IntlDateFormatter

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getCalendar(): int|false
```

Процедурний стиль

```methodsynopsis
datefmt_get_calendar(IntlDateFormatter $formatter): int|false
```

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

[Тип календаря](class.intldateformatter.md#intl.intldateformatter-constants.calendartypes), який використовується сервісом форматування. Або **`IntlDateFormatter::TRADITIONAL`**, або **`IntlDateFormatter::GREGORIAN`**. Повертає **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **datefmtgetcalendar()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Тип календаря средства форматирования : ' . datefmt_get_calendar($fmt);
datefmt_set_calendar($fmt, IntlDateFormatter::TRADITIONAL);
echo 'Теперь тип календаря средства форматирования : ' . datefmt_get_calendar($fmt);
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Тип календаря средства форматирования : ' . $fmt->getCalendar();
$fmt->setCalendar(IntlDateFormatter::TRADITIONAL);
echo 'Теперь тип календаря средства форматирования : ' . $fmt->getCalendar();

?>
```

Результат виконання цього прикладу:

```
Тип календаря средства форматирования : 1
Теперь тип календаря средства форматирования : 0
```

### Дивіться також

-   [datefmtgetcalendarobject()](intldateformatter.getcalendarobject.md) - Отримує копію об'єкта календаря засобу форматування
-   [datefmtsetcalendar()](intldateformatter.setcalendar.md) - Встановлює тип календаря, який використовується засобом форматування
-   [datefmtcreate()](intldateformatter.create.md) - Створює засіб форматування дати
