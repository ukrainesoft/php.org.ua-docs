Отримує ідентифікатор часового поясу, який використовується IntlDateFormatter

-   [« IntlDateFormatter::getTimeType](intldateformatter.gettimetype.html)
    
-   [IntlDateFormatter::getCalendarObject »](intldateformatter.getcalendarobject.html)
    
-   [PHP Manual](index.html)
    
-   [IntlDateFormatter](class.intldateformatter.html)
    
-   Отримує ідентифікатор часового поясу, який використовується IntlDateFormatter
    

# IntlDateFormatter::getTimeZoneId

# datefmtgettimezoneід

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getTimeZoneId -- datefmtgettimezoneid — Отримує ідентифікатор часового поясу, який використовується IntlDateFormatter

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getTimeZoneId(): string|false
```

Процедурний стиль

```methodsynopsis
datefmt_get_timezone_id(IntlDateFormatter $formatter): string|false
```

Отримує ідентифікатор часового поясу, який використовується IntlDateFormatter.

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

Рядок ідентифікатора часового поясу, який використовується цим засобом форматування або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **datefmtgettimezoneid()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'timezone_id средства форматирования: ' . datefmt_get_timezone_id($fmt) . "\n";
datefmt_set_timezone($fmt, 'Europe/Madrid');
echo 'Теперь timezone_id средства форматирования: ' . datefmt_get_timezone_id($fmt);

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
echo 'timezone_id средства форматирования: ' . $fmt->getTimezoneId() . "\n";
$fmt->setTimezone('Europe/Madrid');
echo 'Теперь timezone_id средства форматирования: ' . $fmt->getTimezoneId();

?>
```

Результат виконання цього прикладу:

```
timezone_id средства форматирования: America/Los_Angeles
Теперь timezone_id средства форматирования: Europe/Madrid
```

### Дивіться також

-   [datefmtsettimezone()](intldateformatter.settimezone.html) - Встановлює часовий пояс засобу форматування
-   [datefmtcreate()](intldateformatter.create.html) - Створює засіб форматування дати