---
navigation:
  - intldateformatter.parse.md: '« IntlDateFormatter::parse'
  - intldateformatter.setlenient.md: 'IntlDateFormatter::setLenient »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::setCalendar'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlDateFormatter::setCalendar

# datefmt\_set\_calendar

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::setCalendar -- datefmt\_set\_calendar — Встановлює тип календаря за допомогою форматування.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::setCalendar(IntlCalendar|int|null $calendar): bool
```

Процедурний стиль

```methodsynopsis
datefmt_set_calendar(IntlDateFormatter $formatter, IntlCalendar|int|null $calendar): bool
```

Встановлює тип календаря, який використовується засобом форматування.

### Список параметрів

`formatter`

Ресурс засобу форматування.

`calendar`

Може бути: [тип календаря](class.intldateformatter.md#intl.intldateformatter-constants.calendartypes)для использования (по умолчанию\*\*`IntlDateFormatter::GREGORIAN`\*\*, який також використовується, якщо вказано значення **`null`**) або об'єкт [IntlCalendar](class.intlcalendar.md)

Будь-який переданий об'єкт [IntlCalendar](class.intlcalendar.md) буде клоновано; до об'єкта аргументу не буде внесено жодних змін.

Часовий пояс засобу форматування буде збережено лише в тому випадку, якщо об'єкт [IntlCalendar](class.intlcalendar.md) не переданий, інакше новий часовий пояс буде таким самим, як у переданого об'єкта.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 5.5.0/PECL 3.0.0 | Додана можливість передати об'єкт [IntlCalendar](class.intlcalendar.md) |

### Приклади

**Приклад #1 Приклад використання** datefmt\_set\_calendar()\*\*\*\*

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
echo 'Теперь тип календаря : ' . datefmt_get_calendar($fmt);
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
echo 'Теперь тип календаря : ' . $fmt->getCalendar();
?>
```

Результат виконання наведеного прикладу:

```
Тип календаря средства форматирования : 1
Теперь тип календаря : 0
```

**Приклад #3 Приклад использования[IntlCalendar](class.intlcalendar.md)с параметром**

```php
<?php
$time = strtotime("2013-03-03 00:00:00 UTC");
$formatter = IntlDateFormatter::create("en_US", NULL, NULL, "Europe/Amsterdam");

echo "До: ", $formatter->format($time), "\n";

/* обратите внимание, что языковой стандарт календаря не используется! */
$formatter->setCalendar(IntlCalendar::createInstance(
               "America/New_York", "pt_PT@calendar=islamic"));

echo "После:  ", $formatter->format($time), "\n";
```

Результат виконання наведеного прикладу:

```
До: Sunday, March 3, 2013 at 1:00:00 AM Central European Standard Time
После:  Saturday, Rabiʻ II 20, 1434 at 7:00:00 PM Eastern Standard Time
```

### Дивіться також

-   [datefmt\_get\_calendar()](intldateformatter.getcalendar.md) \- Отримує тип календаря для об'єкта IntlDateFormatter
-   [datefmt\_get\_calendar\_object()](intldateformatter.getcalendarobject.md) \- Отримує копію об'єкта календаря засобу форматування
-   [datefmt\_create()](intldateformatter.create.md) \- Створює засіб форматування дати
