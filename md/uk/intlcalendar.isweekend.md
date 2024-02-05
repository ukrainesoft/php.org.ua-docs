---
navigation:
  - intlcalendar.isset.md: '« IntlCalendar::isSet'
  - intlcalendar.roll.md: 'IntlCalendar::roll »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::isWeekend'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::isWeekend

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::isWeekend — Визначає, чи припадають певні дата/час на вихідні

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::isWeekend(?float $timestamp = null): bool
```

Процедурний стиль

```methodsynopsis
intlcal_is_weekend(IntlCalendar $calendar, ?float $timestamp = null): bool
```

Повертає, чи є поточний час об'єкта чи задана тимчасова мітка вихідними в системі календаря цього об'єкта.

Для цієї функції потрібний ICU 4.4 або новіший.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`timestamp`

Необов'язкова мітка часу, що становить кількість мілісекунд з початку епохи Unix, за винятком додаткових секунд. Якщо **`null`**, натомість використовується поточний час об'єкта.

### Значення, що повертаються

Логічне значення (bool), що вказує на те, чи є час об'єкта вихідними.

У разі виникнення помилки також повертається \*\*`false`\*\*Для обнаружения условий ошибки используйте[intl\_get\_error\_code()](function.intl-get-error-code.md) або настройте викидання [винятків](intl.configuration.md#ini.intl.use-exceptions)в Intl.

### Приклади

**Пример #1 Пример использования**IntlCalendar::isWeekend()\*\*\*\*

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');

$cal = new IntlGregorianCalendar(NULL, 'en_US');
$cal->set(2013, 6 /* Июль */, 7); // Воскресенье

var_dump($cal->isWeekend()); // true
var_dump($cal->isWeekend(strtotime('2013-07-01 00:00:00'))); // false, Понедельник

$cal = new IntlGregorianCalendar(NULL, 'ar_SA');
$cal->set(2013, 6 /* Июль */, 7); // Воскресенье
var_dump($cal->isWeekend()); // false, воскресенье не является выходным днём в этом календаре
```

### Дивіться також

-   [IntlCalendar::getDayOfWeekType()](intlcalendar.getdayofweektype.md) \- Повідомляє, чи є день буднім, вихідним чи днем ​​із переходом між ними
-   [IntlCalendar::getWeekendTransition()](intlcalendar.getweekendtransition.md) \- Отримує час дня, коли вихідні починаються чи закінчуються
