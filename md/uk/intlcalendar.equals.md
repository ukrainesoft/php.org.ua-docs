---
navigation:
  - intlcalendar.createinstance.md: '« IntlCalendar::createInstance'
  - intlcalendar.fielddifference.md: 'IntlCalendar::fieldDifference »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::equals'
---
# IntlCalendar::equals

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::equals — Порівнює час двох об'єктів IntlCalendar щодо рівності

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::equals(IntlCalendar $other): bool
```

Процедурний стиль

```methodsynopsis
intlcal_equals(IntlCalendar $calendar, IntlCalendar $other): bool
```

Повертає true, якщо в обох календарів один і той самий час. Налаштування, типи календаря та стани полів не обов'язково повинні збігатися.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`other`

Календар для порівняння з основним об'єктом.

### Значення, що повертаються

Повертає **`true`**, якщо поточний час цього та переданого в [IntlCalendar](class.intlcalendar.md) об'єкта однакове або **`false`** в іншому випадку.

У разі виникнення помилки також повертається **`false`**. Для виявлення умов помилки використовуйте [intlgeterrorcode()](function.intl-get-error-code.md) або настройте викидання [исключений](intl.configuration.md#ini.intl.use-exceptions) в Intl.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::equals()****

```php
<?php
ini_set('date.timezone', 'UTC');

$cal1 = IntlCalendar::createInstance(NULL, 'es_ES');
$cal2 = clone $cal1;

var_dump($cal1->equals($cal2)); //TRUE

// Языковой стандарт не включён в сравнение
$cal2 = IntlCalendar::createInstance(NULL, 'pt_PT');
$cal2->setTime($cal1->getTime());
var_dump($cal1->equals($cal2)); //TRUE

// И состояние установленных полей также не включено
$cal2->clear(IntlCalendar::FIELD_YEAR);
var_dump($cal1->isSet(IntlCalendar::FIELD_YEAR) ==
        $cal2->isSet(IntlCalendar::FIELD_YEAR)); //FALSE
var_dump($cal1->equals($cal2)); //TRUE

// И тип календаря
$cal2 = IntlCalendar::createInstance(NULL, 'es_ES@calendar=islamic');
$cal2->setTime($cal1->getTime());
var_dump($cal1->equals($cal2)); //TRUE

// Только время
$cal2 = clone $cal1;
$cal2->setTime($cal1->getTime() + 1.);
var_dump($cal1->equals($cal2)); //FALSE
```
