Повертає часовий пояс щодо поточного значення DateTime

-   [« DateTimeInterface::getTimestamp](datetime.gettimestamp.md)
    
-   [DateTime::wakeup »](datetime.wakeup.md)
    
-   [PHP Manual](index.md)
    
-   [DateTimeInterface](class.datetimeinterface.md)
    
-   Повертає часовий пояс щодо поточного значення DateTime
    

# DateTimeInterface::getTimezone

# DateTimeImmutable::getTimezone

# DateTime::getTimezone

# datetimezoneget

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTimeInterface::getTimezone -- DateTimeImmutable::getTimezone -- DateTime::getTimezone -- datetimezoneget — Повертає часовий пояс щодо поточного значення DateTime

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTimeInterface::getTimezone(): DateTimeZone|false
```

```methodsynopsis
public DateTimeImmutable::getTimezone(): DateTimeZone|false
```

```methodsynopsis
public DateTime::getTimezone(): DateTimeZone|false
```

Процедурний стиль

```methodsynopsis
date_timezone_get(DateTimeInterface $object): DateTimeZone|false
```

Повертає часовий пояс щодо поточного значення DateTime.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [datecreate()](function.date-create.html)

### Значення, що повертаються

Повертає об'єкт [DateTimeZone](class.datetimezone.md) у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **DateTime::getTimezone()****

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable(null, new DateTimeZone('Europe/London'));
$tz = $date->getTimezone();
echo $tz->getName();
?>
```

Процедурний стиль

```php
<?php
$date = date_create(null, timezone_open('Europe/London'));
$tz = date_timezone_get($date);
echo timezone_name_get($tz);
?>
```

Результат виконання даних прикладів:

```
Europe/London
```

### Дивіться також

-   [DateTime::setTimezone()](datetime.settimezone.md) - Встановлює часовий пояс для об'єкта класу DateTime