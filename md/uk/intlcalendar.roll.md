---
navigation:
  - intlcalendar.isweekend.md: '« IntlCalendar::isWeekend'
  - intlcalendar.set.md: 'IntlCalendar::set »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::roll'
---
# IntlCalendar::roll

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::roll — Додає значення в поле без перенесення до найважливіших полів

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::roll(int $field, int|bool $value): bool
```

Процедурний стиль

```methodsynopsis
intlcal_roll(IntlCalendar $calendar, int $field, int|bool $value): bool
```

Додає кількість (зі знаком) у поле. Відмінність від [IntlCalendar::add()](intlcalendar.add.md) полягає в тому, що коли значення поля переповнюється, воно не переноситься у найважливіші поля.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.md) [констант](class.intlcalendar.md#intlcalendar.constants) полів типу дата/час. Ціла кількість від `0` до **`IntlCalendar::FIELD_COUNT`**

`value`

Кількість (зі знаком), що додається до поля, **`true`** для згортання (додавання `1`) або **`false`** для скочування вниз (віднімання `1`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::roll()****

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'pt_PT');

$cal = new IntlGregorianCalendar(2013, 5 /* Июнь */, 30);

$cal->add(IntlCalendar::FIELD_DAY_OF_MONTH, 1);
var_dump(IntlDateFormatter::formatObject($cal)); // "01/07/2013, 00:00:00"

$cal->set(2013, 5 /* Июнь */, 30);
$cal->roll(IntlCalendar::FIELD_DAY_OF_MONTH, true); // свернуть так же, как скатиться +1
var_dump(IntlDateFormatter::formatObject($cal)); // "01/06/2013, 00:00:00"
```

Результат виконання цього прикладу:

```
string(20) "01/07/2013, 00:00:00"
string(20) "01/06/2013, 00:00:00"
```

### Дивіться також

-   [IntlCalendar::add()](intlcalendar.add.md) - Додає кількість (зі знаком) часу у полі
-   [IntlCalendar::set()](intlcalendar.set.md) - Встановлює поле часу або одразу кілька спільних полів
