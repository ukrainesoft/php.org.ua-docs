---
navigation:
  - intldateformatter.parse.html: '« IntlDateFormatter::parse'
  - intldateformatter.setlenient.html: 'IntlDateFormatter::setLenient »'
  - index.html: PHP Manual
  - class.intldateformatter.html: IntlDateFormatter
title: 'IntlDateFormatter::setCalendar'
---
# IntlDateFormatter::setCalendar

# datefmtsetcalendar

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::setCalendar -- datefmtsetcalendar — Встановлює тип календаря за допомогою форматування.

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

Може бути: [тип календаря](class.intldateformatter.html#intl.intldateformatter-constants.calendartypes) для використання (за замовчуванням **`IntlDateFormatter::GREGORIAN`**, який також використовується, якщо вказано значення **`null`**) або об'єкт [IntlCalendar](class.intlcalendar.html)

Будь-який переданий об'єкт [IntlCalendar](class.intlcalendar.html) буде клоновано; до об'єкта аргументу не буде внесено жодних змін.

Часовий пояс засобу форматування буде збережено лише в тому випадку, якщо об'єкт [IntlCalendar](class.intlcalendar.html) не переданий, інакше новий часовий пояс буде таким самим, як у переданого об'єкта.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 5.5.0/PECL 3.0.0 | Додана можливість передати об'єкт [IntlCalendar](class.intlcalendar.html) |

### Приклади

**Приклад #1 Приклад використання **datefmtsetcalendar()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Тип календаря средства форматирования : ' . datefmt_get_calendar($fmt);
datefmt_set_calendar($fmt, IntlDateFormatter::TRADITIONAL);
echo 'Теперь тип календаря : ' . datefmt_get_calendar($fmt);
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Тип календаря средства форматирования : ' . $fmt->getCalendar();
$fmt->setCalendar(IntlDateFormatter::TRADITIONAL);
echo 'Теперь тип календаря : ' . $fmt->getCalendar();
?>
```

Результат виконання цього прикладу:

```
Тип календаря средства форматирования : 1
Теперь тип календаря : 0
```

**Приклад #3 Приклад використання [IntlCalendar](class.intlcalendar.html) з параметром**

```php
<?php
$time = strtotime("2013-03-03 00:00:00 UTC");
$formatter = IntlDateFormatter::create("en_US", NULL, NULL, "Europe/Amsterdam");

echo "До: ", $formatter->format($time), "\n";

/* обратите внимание, что языковой стандарт календаря не используется! */
$formatter->setCalendar(IntlCalendar::createInstance(
               "America/New_York", "pt_PT@calendar=islamic"));

echo "После:  ", $formatter->format($time), "\n";
```

Результат виконання цього прикладу:

```
До: Sunday, March 3, 2013 at 1:00:00 AM Central European Standard Time
После:  Saturday, Rabiʻ II 20, 1434 at 7:00:00 PM Eastern Standard Time
```

### Дивіться також

-   [datefmtgetcalendar()](intldateformatter.getcalendar.html) - Отримує тип календаря, який використовується IntlDateFormatter
-   [datefmtgetcalendarobject()](intldateformatter.getcalendarobject.html) - Отримує копію об'єкта календаря засобу форматування
-   [datefmtcreate()](intldateformatter.create.html) - Створює засіб форматування дати
