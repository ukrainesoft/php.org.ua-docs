---
navigation:
  - datetimezone.construct.md: '« DateTimeZone::\_\_construct'
  - datetimezone.getname.md: 'DateTimeZone::getName »'
  - index.md: PHP Manual
  - class.datetimezone.md: DateTimeZone
title: 'DateTimeZone::getLocation'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTimeZone::getLocation

# timezone\_location\_get

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DateTimeZone::getLocation -- timezone\_location\_get — Повертає інформацію про місцезнаходження для часового поясу

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

Тільки для процедурного стилю: об'єкт [DateTimeZone](class.datetimezone.md), що повертається [timezone\_open()](function.timezone-open.md)

### Значення, що повертаються

Массив, содержащий информацию о местоположении часового пояса или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** DateTimeZone::getLocation()\*\*\*\*

```php
<?php
$tz = new DateTimeZone("Europe/Prague");
print_r($tz->getLocation());
print_r(timezone_location_get($tz));
?>
```

Результат виконання наведеного прикладу:

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

-   Функция[DateTimeZone::listIdentifiers()](datetimezone.listidentifiers.md) \- Повертає чисельно індексований масив з усіма ідентифікаторами часових поясів для отримання повного або часткового списку всіх ідентифікаторів часових поясів, що підтримуються.
