---
navigation:
  - intlcalendar.equals.md: '« IntlCalendar::equals'
  - intlcalendar.fromdatetime.md: 'IntlCalendar::fromDateTime »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::fieldDifference'
---
# IntlCalendar::fieldDifference

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::fieldDifference — Обчислює різницю між заданим часом та часом об'єкта

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::fieldDifference(float $timestamp, int $field): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_field_difference(IntlCalendar $calendar, float $timestamp, int $field): int|false
```

Повертає різницю між заданим часом та часом, встановленим для об'єкта, щодо кількості, зазначеної у параметрі `field`

Метод призначений для послідовного виклику, в першу чергу від найбільш значущою областю інтересів до найменш значущої області. Як побічний ефект, значення календаря для вказаного поля збільшується на повернену суму.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`timestamp`

Час, з яким порівнюється кількість, представлена `field`. Щоб результат був позитивним, час, вказаний у цьому параметрі, повинен випереджати час об'єкта, якого викликається метод.

`field`

Поле, що становить кількість, що порівнюється.

Одна з представлених у класі [IntlCalendar](class.intlcalendar.md) [констант](class.intlcalendar.md#intlcalendar.constants) полів типу дата/час. Ціла кількість від `0` до **`IntlCalendar::FIELD_COUNT`**

### Значення, що повертаються

Повертає різницю часу (зі знаком) в одиницях виміру, пов'язаних із зазначеним полем або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::fieldDifference()****

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'fr_FR');

$cal1 = IntlCalendar::fromDateTime('2012-02-29 09:00:11');
$cal2 = IntlCalendar::fromDateTime('2013-03-01 09:19:29');
$time = $cal2->getTime();

echo "Время до: ", IntlDateFormatter::formatObject($cal1), "\n";

printf(
    "Разница во времени: %d год(лет), %d месяц(ев), "
  . "%d день(дней), %d час(ов) и %d минуту(минут)\n",
    $cal1->fieldDifference($time, IntlCalendar::FIELD_YEAR),
    $cal1->fieldDifference($time, IntlCalendar::FIELD_MONTH),
    $cal1->fieldDifference($time, IntlCalendar::FIELD_DAY_OF_MONTH),
    $cal1->fieldDifference($time, IntlCalendar::FIELD_HOUR_OF_DAY),
    $cal1->fieldDifference($time, IntlCalendar::FIELD_MINUTE)
);

// теперь оно было продвинуто к целевому времени, за исключением секунд,
// для которых мы не измеряли разницу
echo "Время после: ", IntlDateFormatter::formatObject($cal1), "\n";
```

Результат виконання цього прикладу:

```
Время до: 29 févr. 2012 09:00:11
Разница во времени: 1 год(лет), 0 месяц(ев), 1 день(дней), 0 час(ов) and 19 минуту(минут)
Время после: 1 mars 2013 09:19:11
```
