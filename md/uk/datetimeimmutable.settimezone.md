Встановлює часовий пояс

-   [« DateTimeImmutable::setTimestamp](datetimeimmutable.settimestamp.html)
    
-   [DateTimeImmutable::sub »](datetimeimmutable.sub.html)
    
-   [PHP Manual](index.html)
    
-   [DateTimeImmutable](class.datetimeimmutable.html)
    
-   Встановлює часовий пояс
    

# DateTimeImmutable::setTimezone

(PHP 5> = 5.5.0, PHP 7, PHP 8)

DateTimeImmutable::setTimezone — Встановлює часовий пояс

### Опис

```methodsynopsis
public DateTimeImmutable::setTimezone(DateTimeZone $timezone): DateTimeImmutable
```

Повертає новий об'єкт DateTimeImmutable із встановленим новим часовим поясом.

### Список параметрів

`timezone`

Об'єкт [DateTimeZone](class.datetimezone.html), що представляє бажаний часовий пояс.

### Значення, що повертаються

Повертає новий модифікований об'єкт [DateTimeImmutable](class.datetimeimmutable.html) для ланцюжка методів. момент часу, що лежить в основі, не змінюється при виклику методу.

### Приклади

**Приклад #1 Приклад використання **DateTimeImmutable::setTimeZone()****

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable('2000-01-01', new DateTimeZone('Pacific/Nauru'));
echo $date->format('Y-m-d H:i:sP') . "\n";

$newDate = $date->setTimezone(new DateTimeZone('Pacific/Chatham'));
echo $newDate->format('Y-m-d H:i:sP') . "\n";
?>
```

Результат виконання даних прикладів:

```
2000-01-01 00:00:00+12:00
2000-01-01 01:45:00+13:45
```

### Дивіться також

-   [DateTimeImmutable::getTimezone()](datetime.gettimezone.html) - Повертає часовий пояс щодо поточного значення DateTime
-   [DateTimeZone::construct()](datetimezone.construct.html) - Створює новий об'єкт DateTimeZone