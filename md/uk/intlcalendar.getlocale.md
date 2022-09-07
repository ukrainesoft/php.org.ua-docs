---
navigation:
  - intlcalendar.getleastmaximum.md: '« IntlCalendar::getLeastMaximum'
  - intlcalendar.getmaximum.md: 'IntlCalendar::getMaximum »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getLocale'
---
# IntlCalendar::getLocale

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getLocale — Отримує мовний стандарт, пов'язаний з об'єктом

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getLocale(int $type): string|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_locale(IntlCalendar $calendar, int $type): string|false
```

Повертає мовний стандарт, пов'язаний із об'єктом.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`type`

Чи слід отримувати фактичний мовний стандарт (мовний стандарт, з якого походять дані календаря, за допомогою **`Locale::ACTUAL_LOCALE`**) чи дійсний мовний стандарт, т.к. найбільш конкретний мовний стандарт, що підтримується ICU щодо запитаного мовного стандарту - дивіться **`Locale::VALID_LOCALE`**. Від найбільш загальних до найчастіших, мовні стандарти відсортовані в такий спосіб: фактичний мовний стандарт, допустимий мовний стандарт, запитаний мовний стандарт.

### Значення, що повертаються

Мовний стандарт у вигляді рядка або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::getLocale()****

```php
<?php
$cal = IntlCalendar::createInstance(IntlTimeZone::getGMT(), 'en_US_CALIFORNIA');
var_dump(
    $cal->getLocale(Locale::ACTUAL_LOCALE),
    $cal->getLocale(Locale::VALID_LOCALE)
);
```

Результат виконання цього прикладу:

```
string(2) "en"
string(5) "en_US"
```
