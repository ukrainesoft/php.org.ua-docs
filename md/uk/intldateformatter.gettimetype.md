Отримує тип часу, який використовується IntlDateFormatter

-   [« IntlDateFormatter::getPattern](intldateformatter.getpattern.html)
    
-   [IntlDateFormatter::getTimeZoneId »](intldateformatter.gettimezoneid.html)
    
-   [PHP Manual](index.html)
    
-   [IntlDateFormatter](class.intldateformatter.html)
    
-   Отримує тип часу, який використовується IntlDateFormatter
    

# IntlDateFormatter::getTimeType

# datefmtgettimetype

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getTimeType -- datefmtgettimetype — Отримує тип часу, який використовується IntlDateFormatter

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getTimeType(): int|false
```

Процедурний стиль

```methodsynopsis
datefmt_get_timetype(IntlDateFormatter $formatter): int|false
```

Повертає тип часу, який використовується засобом форматування.

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

Значення поточного [типа даты](class.intldateformatter.html#intl.intldateformatter-constants) засоби форматування або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **datefmtgettimetype()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Тип времени средства форматирования : ' . datefmt_get_timetype($fmt);
echo 'Первый отформатированный вывод ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::SHORT,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Теперь тип времени средства форматирования : ' . datefmt_get_timetype($fmt);
echo 'Второй отформатированный вывод ' . datefmt_format($fmt, 0);

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
echo 'Тип времени средства форматирования : ' . $fmt->getTimeType();
echo 'Первый отформатированный вывод ' . $fmt->format(0);

$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::SHORT,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Теперь тип времени средства форматирования : ' . $fmt->getTimeType();
echo 'Второй отформатированный вывод ' . $fmt->format(0);

?>
```

Результат виконання цього прикладу:

```
Тип времени средства форматирования : 0
Первый отформатированный вывод Wednesday, December 31, 1969 4:00:00 PM PT
Теперь тип времени средства форматирования : 3
Второй отформатированный вывод Wednesday, December 31, 1969 4:00 PM
```

### Дивіться також

-   [datefmt\_get\_datetype()](intldateformatter.getdatetype.html) - Отримує тип дати, що використовується IntlDateFormatter
-   [datefmt\_create()](intldateformatter.create.html) - Створює засіб форматування дати