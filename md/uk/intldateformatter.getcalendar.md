Отримує тип календаря, який використовується IntlDateFormatter

-   [« IntlDateFormatter::formatObject](intldateformatter.formatobject.html)
    
-   [IntlDateFormatter::getDateType »](intldateformatter.getdatetype.html)
    
-   [PHP Manual](index.html)
    
-   [IntlDateFormatter](class.intldateformatter.html)
    
-   Отримує тип календаря, який використовується IntlDateFormatter
    

# IntlDateFormatter::getCalendar

# datefmtgetcalendar

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getCalendar -- datefmtgetcalendar — Отримує тип календаря, який використовується IntlDateFormatter

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getCalendar(): int|false
```

Процедурний стиль

```methodsynopsis
datefmt_get_calendar(IntlDateFormatter $formatter): int|false
```

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

[Тип календаря](class.intldateformatter.html#intl.intldateformatter-constants.calendartypes), який використовується сервісом форматування. Або **`IntlDateFormatter::TRADITIONAL`**, або **`IntlDateFormatter::GREGORIAN`**. Повертає **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **datefmtgetcalendar()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Тип календаря средства форматирования : ' . datefmt_get_calendar($fmt);
datefmt_set_calendar($fmt, IntlDateFormatter::TRADITIONAL);
echo 'Теперь тип календаря средства форматирования : ' . datefmt_get_calendar($fmt);
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
echo 'Тип календаря средства форматирования : ' . $fmt->getCalendar();
$fmt->setCalendar(IntlDateFormatter::TRADITIONAL);
echo 'Теперь тип календаря средства форматирования : ' . $fmt->getCalendar();

?>
```

Результат виконання цього прикладу:

```
Тип календаря средства форматирования : 1
Теперь тип календаря средства форматирования : 0
```

### Дивіться також

-   [datefmt\_get\_calendar\_object()](intldateformatter.getcalendarobject.html) - Отримує копію об'єкта календаря засобу форматування
-   [datefmt\_set\_calendar()](intldateformatter.setcalendar.html) - Встановлює тип календаря, який використовується засобом форматування
-   [datefmt\_create()](intldateformatter.create.html) - Створює засіб форматування дати