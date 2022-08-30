Повертає інформацію про місцезнаходження для часового поясу

-   [« DateTimeZone::construct](datetimezone.construct.html)
    
-   [DateTimeZone::getName »](datetimezone.getname.html)
    
-   [PHP Manual](index.html)
    
-   [DateTimeZone](class.datetimezone.html)
    
-   Повертає інформацію про місцезнаходження для часового поясу
    

# DateTimeZone::getLocation

# timezonelocationget

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateTimeZone::getLocation -- timezonelocationget — Повертає інформацію про місцезнаходження для часового поясу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTimeZone::getLocation(): array|false
```

Процедурний стиль

```methodsynopsis
timezone_location_get(DateTimeZone $object): array|false
```

Повертає інформацію про місцезнаходження часового поясу, включаючи код країни, широту/довготу та коментарі.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTimeZone](class.datetimezone.html), що повертається [timezoneopen()](function.timezone-open.html)

### Значення, що повертаються

Масив, що містить інформацію про місцезнаходження часового поясу або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **DateTimeZone::getLocation()****

```php
<?php
$tz = new DateTimeZone("Europe/Prague");
print_r($tz->getLocation());
print_r(timezone_location_get($tz));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [country_code] => CZ
    [latitude] => 50.08333
    [longitude] => 14.43333
    [comments] =>
)
Array
(
    [country_code] => CZ
    [latitude] => 50.08333
    [longitude] => 14.43333
    [comments] =>
)
```

### Дивіться також

-   Функція [DateTimeZone::listIdentifiers()](datetimezone.listidentifiers.html) - Повертає чисельно індексований масив з усіма ідентифікаторами часових поясів для отримання повного або часткового списку всіх ідентифікаторів часових поясів, що підтримуються.