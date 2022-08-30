Отримує тип дати, який використовується IntlDateFormatter

-   [« IntlDateFormatter::getCalendar](intldateformatter.getcalendar.html)
    
-   [IntlDateFormatter::getErrorCode »](intldateformatter.geterrorcode.html)
    
-   [PHP Manual](index.html)
    
-   [IntlDateFormatter](class.intldateformatter.html)
    
-   Отримує тип дати, який використовується IntlDateFormatter
    

# IntlDateFormatter::getDateType

# datefmtgetdatetype

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getDateType -- datefmtgetdatetype — Отримує тип дати, який використовується IntlDateFormatter

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getDateType(): int|false
```

Процедурний стиль

```methodsynopsis
datefmt_get_datetype(IntlDateFormatter $formatter): int|false
```

Отримує тип дати, який використовується засобом форматування.

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

Значення поточного [типу дати](class.intldateformatter.html#intl.intldateformatter-constants) засоби форматування або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **datefmtgetdatetype()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Тип даты средства форматирования : ' . datefmt_get_datetype($fmt);
echo 'Первый отформатированный вывод с типом даты ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::SHORT,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Теперь тип даты средства форматирования : ' . datefmt_get_datetype($fmt);
echo 'Второй отформатированный вывод с типом даты ' . datefmt_format($fmt, 0);

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
echo 'Тип даты средства форматирования : ' . $fmt->getDateType();
echo 'Первый отформатированный вывод с типом даты ' . $fmt->format(0);
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::SHORT,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Теперь тип даты средства форматирования : ' . $fmt->getDateType();
echo 'Второй отформатированный вывод с типом даты ' . $fmt->format(0);

?>
```

Результат виконання цього прикладу:

```
Тип даты средства форматирования : 0
Первый отформатированный вывод с типом даты Wednesday, December 31, 1969 4:00:00 PM PT
Теперь тип даты средства форматирования : 2
Второй отформатированный вывод с типом даты 12/31/69 4:00:00 PM PT
```

### Дивіться також

-   [datefmtgettimetype()](intldateformatter.gettimetype.html) - Отримує тип часу, який використовується IntlDateFormatter
-   [datefmtcreate()](intldateformatter.create.html) - Створює засіб форматування дати