Встановлює часовий пояс засобу форматування

-   [« IntlDateFormatter::setPattern](intldateformatter.setpattern.html)
    
-   [ResourceBundle »](class.resourcebundle.html)
    
-   [PHP Manual](index.html)
    
-   [IntlDateFormatter](class.intldateformatter.html)
    
-   Встановлює часовий пояс засобу форматування
    

# IntlDateFormatter::setTimeZone

# datefmtsettimezone

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL intl >= 3.0.0)

IntlDateFormatter::setTimeZone -- datefmtsettimezone — Встановлює часовий пояс засобу форматування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::setTimeZone(IntlTimeZone|DateTimeZone|string|null $timezone): ?bool
```

Процедурний стиль

```methodsynopsis
datefmt_set_timezone(IntlDateFormatter $formatter, IntlTimeZone|DateTimeZone|string|null $timezone): ?bool
```

Встановлює часовий пояс, який використовується об'єктом IntlDateFormatter.

### Список параметрів

`formatter`

Ресурс засобу форматування.

`timezone`

Часовий пояс для засобу форматування. Можна вказати у таких форматах:

-   Якщо **`null`**, то буде використаний часовий пояс за замовчуванням, задана в ini-налаштування [date.timezone](datetime.configuration.html#ini.date.timezone) або за допомогою функції [date\_default\_timezone\_set()](function.date-default-timezone-set.html) та повернена функцією [date\_default\_timezone\_get()](function.date-default-timezone-get.html)
    
-   Об'єкт класу [IntlTimeZone](class.intltimezone.html)
    
-   Об'єкт класу [DateTimeZone](class.datetimezone.html). Його ідентифікатор буде вилучено і на його основі буде створено об'єкт часового поясу ICU; часовий пояс буде збережено в базі даних ICU, а не PHP.
    
-   Рядок є коректним ідентифікатором часового поясу ICU. Дивіться [IntlTimeZone::createTimeZoneIDEnumeration()](intltimezone.createtimezoneidenumeration.html). "Сирі" усунення, типу `"GMT+08:30"`, також підтримуються.
    

### Значення, що повертаються

Повертає **`null`** у разі успішного виконання та **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlDateFormatter::setTimeZone()****

```php
<?php
ini_set('date.timezone', 'Europe/Amsterdam');

$formatter = IntlDateFormatter::create(NULL, NULL, NULL, "UTC");

$formatter->setTimeZone(NULL);
echo "NULL\n    ", $formatter->getTimeZone()->getId(), "\n";

$formatter->setTimeZone(IntlTimeZone::createTimeZone('Europe/Lisbon'));
echo "IntlTimeZone\n    ", $formatter->getTimeZone()->getId(), "\n";

$formatter->setTimeZone(new DateTimeZone('Europe/Paris'));
echo "DateTimeZone\n    ", $formatter->getTimeZone()->getId(), "\n";

$formatter->setTimeZone('Europe/Rome');
echo "String\n    ", $formatter->getTimeZone()->getId(), "\n";

$formatter->setTimeZone('GMT+00:30');
print_r($formatter->getTimeZone());
```

Результат виконання цього прикладу:

```
NULL
    Europe/Amsterdam
IntlTimeZone
    Europe/Lisbon
DateTimeZone
    Europe/Paris
String
    Europe/Rome
IntlTimeZone Object
(
    [valid] => 1
    [id] => GMT+00:30
    [rawOffset] => 1800000
    [currentOffset] => 1800000
)
```

### Дивіться також

-   [IntlDateFormatter::getTimeZone()](intldateformatter.gettimezone.html) - Отримує часовий пояс засобу форматування