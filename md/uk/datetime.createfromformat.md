Розбирає рядок з датою згідно з вказаним форматом

-   [« DateTime::construct](datetime.construct.html)
    
-   [DateTime::createFromImmutable »](datetime.createfromimmutable.html)
    
-   [PHP Manual](index.html)
    
-   [DateTime](class.datetime.html)
    
-   Розбирає рядок з датою згідно з вказаним форматом
    

# DateTime::createFromFormat

# datecreatefromformat

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateTime::createFromFormat -- datecreatefromformat — Розбирає рядок з датою згідно з вказаним форматом

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static DateTime::createFromFormat(string $format, string $datetime, ?DateTimeZone $timezone = null): DateTime|false
```

Процедурний стиль

```methodsynopsis
date_create_from_format(string $format, string $datetime, ?DateTimeZone $timezone = null): DateTime|false
```

Повертає новий об'єкт DateTime, що представляє дату та час, задані рядком `datetime`, яка була відформатована у зазначеному `format`

Подібний до методу [DateTimeImmutable::createFromFormat()](datetimeimmutable.createfromformat.html), крім роботи з об'єктом [DateTime](class.datetime.html)

Процедурна версія приймає об'єкт [DateTime](class.datetime.html) як перший аргумент.

### Список параметрів

Дивіться параметри та їх опис на сторінці методу [DateTimeImmutable::createFromFormat](datetimeimmutable.createfromformat.html)

### Значення, що повертаються

Повертає створений екземпляр класу DateTime або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DateTimeImmutable::createFromFormat()](datetimeimmutable.createfromformat.html) - Розбирає рядок з датою згідно з вказаним форматом