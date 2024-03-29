---
navigation:
  - intlcalendar.gettimezone.md: '« IntlCalendar::getTimeZone'
  - intlcalendar.getweekendtransition.md: 'IntlCalendar::getWeekendTransition »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::getType

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getType — Отримує тип календаря

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getType(): string
```

Процедурний стиль

```methodsynopsis
intlcal_get_type(IntlCalendar $calendar): string
```

Рядок, що описує тип календаря. Одне з [допустимих значень](intlcalendar.getkeywordvaluesforlocale.md) для значення ключового слова календаря `'calendar'`

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

### Значення, що повертаються

Строка (string), представляющая тип календаря, наПриклад,`'gregorian'` `'islamic'`и т.д.

### Приклади

**Приклад #1 Приклад використання** IntlCalendar::getType()\*\*\*\*

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'en_US');

$cal = IntlCalendar::createInstance(NULL, '@calendar=ethiopic-amete-alem');
var_dump($cal->getType());

$cal = new IntlGregorianCalendar();
var_dump($cal->getType());
```

Результат виконання наведеного прикладу:

```
string(19) "ethiopic-amete-alem"
string(9) "gregorian"
```
