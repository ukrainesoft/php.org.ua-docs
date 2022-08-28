Встановлює часовий пояс для об'єкта класу DateTime

-   [« DateTime::setTimestamp](datetime.settimestamp.html)
    
-   [DateTime::sub »](datetime.sub.html)
    
-   [PHP Manual](index.html)
    
-   [DateTime](class.datetime.html)
    
-   Встановлює часовий пояс для об'єкта класу DateTime
    

# DateTime::setTimezone

# datetimezoneset

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTime::setTimezone -- datetimezoneset — Встановлює часовий пояс для об'єкта класу DateTime

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::setTimezone(DateTimeZone $timezone): DateTime
```

Процедурний стиль

```methodsynopsis
date_timezone_set(DateTime $object, DateTimeZone $timezone): DateTime
```

Встановлює новий часовий пояс для об'єкта (object) [DateTime](class.datetime.html)

Подібний до методу [DateTimeImmutable::setTimezone()](datetimeimmutable.settimezone.html), крім роботи з об'єктом [DateTime](class.datetime.html)

Процедурна версія приймає об'єкт [DateTime](class.datetime.html) як перший аргумент.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.html), що повертається [date\_create()](function.date-create.html). Функція змінює цей об'єкт.

`timezone`

Об'єкт класу [DateTimeZone](class.datetimezone.html), що представляє необхідний часовий пояс.

### Значення, що повертаються

Повертає об'єкт [DateTime](class.datetime.html) для зв'язування методів. Момент часу, що лежить в основі, не змінюється при виклику методу.

### Приклади

**Приклад #1 Приклад використання **DateTime::setTimeZone()****

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTime('2000-01-01', new DateTimeZone('Pacific/Nauru'));
echo $date->format('Y-m-d H:i:sP') . "\n";

$date->setTimezone(new DateTimeZone('Pacific/Chatham'));
echo $date->format('Y-m-d H:i:sP') . "\n";
?>
```

Процедурний стиль

```php
<?php
$date = date_create('2000-01-01', timezone_open('Pacific/Nauru'));
echo date_format($date, 'Y-m-d H:i:sP') . "\n";

date_timezone_set($date, timezone_open('Pacific/Chatham'));
echo date_format($date, 'Y-m-d H:i:sP') . "\n";
?>
```

Результат виконання даних прикладів:

```
2000-01-01 00:00:00+12:00
2000-01-01 01:45:00+13:45
```

### Дивіться також

-   [DateTimeImmutable::setTimezone()](datetimeimmutable.settimezone.html) - Встановлює часовий пояс
-   [DateTime::getTimezone()](datetime.gettimezone.html) - Повертає часовий пояс щодо поточного значення DateTime
-   [DateTimeZone::\_\_construct()](datetimezone.construct.html) - Створює новий об'єкт DateTimeZone