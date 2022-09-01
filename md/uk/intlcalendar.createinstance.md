---
navigation:
  - intlcalendar.construct.md: '« IntlCalendar::construct'
  - intlcalendar.equals.md: 'IntlCalendar::equals »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::createInstance'
---
# IntlCalendar::createInstance

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::createInstance — Створює новий об'єкт IntlCalendar

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static IntlCalendar::createInstance(IntlTimeZone|DateTimeZone|string|null $timezone = null, ?string $locale = null): ?IntlCalendar
```

Процедурний стиль

```methodsynopsis
intlcal_create_instance(IntlTimeZone|DateTimeZone|string|null $timezone = null, ?string $locale = null): ?IntlCalendar
```

Враховуючи часовий пояс та мовний стандарт, метод створює об'єкт [IntlCalendar](class.intlcalendar.md). Цей фабричний метод може повертати дочірній клас [IntlCalendar](class.intlcalendar.md)

Створений календар представлятиме момент часу, коли він був створений, на основі системного часу. Усі поля можна очистити, викликавши **IntCalendar::clear()** без аргументів. Дивіться також [IntlGregorianCalendar::construct()](intlgregoriancalendar.construct.md)

### Список параметрів

`timezone`

Часовий пояс для використання.

-   Якщо **`null`**, то буде використаний часовий пояс за замовчуванням, задана в ini-налаштування [date.timezone](datetime.configuration.html#ini.date.timezone) або за допомогою функції [datedefaulttimezoneset()](function.date-default-timezone-set.html) та повернена функцією [datedefaulttimezoneget()](function.date-default-timezone-get.html)
    
-   Об'єкт класу [IntlTimeZone](class.intltimezone.md)
    
-   Об'єкт класу [DateTimeZone](class.datetimezone.md). Його ідентифікатор буде вилучено і на його основі буде створено об'єкт часового поясу ICU; часовий пояс буде збережено в базі даних ICU, а не PHP.
    
-   Рядок є коректним ідентифікатором часового поясу ICU. Дивіться [IntlTimeZone::createTimeZoneIDEnumeration()](intltimezone.createtimezoneidenumeration.md). "Сирі" усунення, типу `"GMT+08:30"`, також підтримуються.
    

`locale`

Використовуваний мовний стандарт або значення **`null`** для використання [мовного стандарту за замовчуванням](intl.configuration.html#ini.intl.default-locale)

### Значення, що повертаються

Створений екземпляр [IntlCalendar](class.intlcalendar.md) або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::createInstance()****

```php
<?php
ini_set('intl.default_locale', 'es_ES');
ini_set('date.timezone', 'Europe/Madrid');

$cal = IntlCalendar::createInstance();
echo "Без аргументов\n";
var_dump(get_class($cal),
        IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL));
echo "\n";

echo "Явное указание часового пояса\n";
$cal = IntlCalendar::createInstance(IntlTimeZone::getGMT());
var_dump(get_class($cal),
        IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL));
echo "\n";

echo "Явное указание языкового стандарта (с календарём)\n";
$cal = IntlCalendar::createInstance(NULL, 'es_ES@calendar=persian');
var_dump(get_class($cal),
        IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL));
```

Результат виконання цього прикладу:

```
Без аргументов
string(21) "IntlGregorianCalendar"
string(68) "martes 18 de junio de 2013 14:11:02 Hora de verano de Europa Central"

Явное указание часового пояса
string(21) "IntlGregorianCalendar"
string(45) "martes 18 de junio de 2013 12:11:02 GMT+00:00"

Явное указание языкового стандарта (с календарём)
string(12) "IntlCalendar"
string(70) "martes 28 de Khordad de 1392 14:11:02 Hora de verano de Europa Central"
```

### Дивіться також

-   [IntlGregorianCalendar::construct()](intlgregoriancalendar.construct.md) - Конструктор класу григоріанського календаря
