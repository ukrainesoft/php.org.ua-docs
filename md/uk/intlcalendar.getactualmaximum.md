---
navigation:
  - intlcalendar.get.html: '« IntlCalendar::get'
  - intlcalendar.getactualminimum.html: 'IntlCalendar::getActualMinimum »'
  - index.html: PHP Manual
  - class.intlcalendar.html: IntlCalendar
title: 'IntlCalendar::getActualMaximum'
---
# IntlCalendar::getActualMaximum

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getActualMaximum — Максимальне значення для поля з урахуванням поточного часу об'єкта

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getActualMaximum(int $field): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_actual_maximum(IntlCalendar $calendar, int $field): int|false
```

Повертає відносне значення поля для поточного часу. Точна семантика залежить від поля, але в загальному випадку це значення, яке було б отримано, якщо встановити значення поля на [найменший відносний максимум](intlcalendar.getleastmaximum.html) і збільшувати його до тих пір, поки не буде досягнуто [глобальний максимум](intlcalendar.getmaximum.html), щоб обернути значення поля, в якому значення, що повертається буде глобальним максимумом або значенням до перенесення, відповідно.

Наприклад, у григоріанському календарі фактичне максимальне значення для [дня месяца](class.intlcalendar.html#intlcalendar.constants.field-day-of-month) варіюватиметься від `28` до `31`, в залежності від місяця та року поточного часу.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.html) [констант](class.intlcalendar.html#intlcalendar.constants) полів типу дата/час. Ціла кількість від `0` до **`IntlCalendar::FIELD_COUNT`**

### Значення, що повертаються

Ціле число (int), що становить максимальне значення в одиницях вимірювання, пов'язане з даними `field` або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::getActualMaximum()****

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');

$cal = IntlCalendar::fromDateTime('2013-02-15');
var_dump($cal->getActualMaximum(IntlCalendar::FIELD_DAY_OF_MONTH)); //28

$cal->add(IntlCalendar::FIELD_EXTENDED_YEAR, -1);
var_dump($cal->getActualMaximum(IntlCalendar::FIELD_DAY_OF_MONTH)); //29
```

Результат виконання цього прикладу:

```
int(28)
int(29)
```

### Дивіться також

-   [IntlCalendar::getMaximum()](intlcalendar.getmaximum.html) - Отримує глобальне максимальне значення поля
-   [IntlCalendar::getLeastMaximum()](intlcalendar.getleastmaximum.html) - Отримує найменший локальний максимум для поля
-   [IntlCalendar::getActualMinimum()](intlcalendar.getactualminimum.html) - Мінімальне значення для поля з урахуванням поточного часу об'єкта
