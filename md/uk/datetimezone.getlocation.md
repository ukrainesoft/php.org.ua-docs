- [« DateTimeZone::\_\_construct](datetimezone.construct.md)
- [DateTimeZone::getName »](datetimezone.getname.md)

- [PHP Manual](index.md)
- [DateTimeZone](class.datetimezone.md)
- Повертає інформацію про місцезнаходження для часового поясу

# DateTimeZone::getLocation

#timezone_location_get

(PHP 5 \>= 5.3.0, PHP 7, PHP 8)

DateTimeZone::getLocation -- timezone_location_get — Повертає
інформацію про місцезнаходження для часового поясу

### Опис

Об'єктно-орієнтований стиль

public **DateTimeZone::getLocation**(): array\|false

Процедурний стиль

[timezone_location_get](function.timezone-location-get.md)([DateTimeZone](class.datetimezone.md)
`$object`): array\|false

Повертає інформацію про місцезнаходження часового поясу, включаючи код
країни, широту/довготу та коментарі.

### Список параметрів

`object`
Тільки для процедурного стилю: об'єкт
[DateTimeZone](class.datetimezone.md), що повертається
[timezone_open()](function.timezone-open.md).

### Значення, що повертаються

Масив, що містить інформацію про місцезнаходження часового поясу або
**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **DateTimeZone::getLocation()****

` <?php$tz = new DateTimeZone("Europe/Prague");print_r($tz->getLocation());print_r(timezone_location_get($tz));?> `

Результат виконання цього прикладу:

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
