---
navigation:
  - function.date-sunrise.md: « datesunrise
  - function.date-time-set.md: datetimeset »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: datesunset
---
# datesunset

(PHP 5, PHP 7, PHP 8)

datesunset — Повертає час заходу сонця для заданого дня та місця розташування

**Увага**

Функція оголошена *Застарілої*починаючи з PHP 8.1.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
date_sunset(    int $timestamp,    int $returnFormat = SUNFUNCS_RET_STRING,    ?float $latitude = null,    ?float $longitude = null,    ?float $zenith = null,    ?float $utcOffset = null): string|int|float|false
```

**datesunset()** повертає час заходу сонця для певних днів (заданого аргументом `timestamp`) та місця розташування.

### Список параметрів

`timestamp`

Тимчасова мітка (`timestamp`) Дня, для якого визначається час заходу сонця.

`returnFormat`

**Константи `returnFormat`**

| константа | описание | пример |
| --- | --- | --- |
| SUNFUNCSRETSTRING | тип результату, що повертається string |  |
| SUNFUNCSRETDOUBLE | тип повертається результату float |  |
| SUNFUNCSRETTIMESTAMP | тип повертається результату int (тимчасова мітка) |  |

`latitude`

За замовчуванням у Північній півкулі для Південної передається негативна величина. Дивіться також [date.defaultlatitude](datetime.configuration.md#ini.date.default-latitude)

`longitude`

За замовчуванням східна для вказівки західної довготи передається негативна величина. Дивіться також [date.defaultlongitude](datetime.configuration.md#ini.date.default-longitude)

`zenith`

`zenith` - це кут між центром Сонця та лінією, перпендикулярної поверхні Землі. За замовчуванням [date.sunsetzenith](datetime.configuration.md#ini.date.sunset-zenith)

**Поширені кути `zenith`**

| Угол | Описание |
| --- | --- |
|  | Схід сонця: точка, де Сонце стає невидимим. |
|  | Цивільні сутінки: зазвичай використовуються для позначення кінця заходу сонця. |
|  | Навігаційні сутінки: точка, в якій обрій стає невидимим з моря. |
|  | Астрономічний сутінки: точка, в якій Сонце закінчує бути джерелом будь-якого освітлення. |

`utcOffset`

Задається в годиннику . `utcOffset` ігнорується, якщо `returnFormat` **`SUNFUNCS_RET_TIMESTAMP`**

### Значення, що повертаються

Повертає час заходу сонця у заданому форматі `returnFormat` або **`false`** у разі виникнення помилки. Одна з можливих причин невдалого виконання – сонце не піднімається над обрієм взагалі, що відбувається всередині полярних кіл протягом частини року.

### Помилки

Кожен виклик до функцій дати/часу при неправильних налаштуваннях часового поясу згенерує помилку рівня **`E_WARNING`**, якщо часовий пояс неправильний. Дивіться також [datedefaulttimezoneset()](function.date-default-timezone-set.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція оголошена застарілою, використовуйте її разом [datesuninfo()](function.date-sun-info.md) |
|  | `latitude` `longitude` `zenith` і `utcOffset` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **datesunset()****

```php
<?php

/* calculate the sunset time for Lisbon, Portugal
Latitude: 38.4 North
Longitude: 9 West
Zenith ~= 90
offset: +1 GMT
*/

echo date("D M d Y"). ', время захода солнца : ' .date_sunset(time(), SUNFUNCS_RET_STRING, 38.4, -9, 90, 1);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Mon Dec 20 2004, время захода солнца : 18:13
```

**Приклад #2 Немає заходу сонця**

```php
<?php
$solstice = strtotime('2017-12-21');
var_dump(date_sunset($solstice, SUNFUNCS_RET_STRING, 69.245833, -53.537222));
?>
```

Результат виконання цього прикладу:

```
bool(false)
```

### Дивіться також

-   [datesunrise()](function.date-sunrise.md) - Повертає час світанку для заданого дня та місця розташування
-   [datesuninfo()](function.date-sun-info.md) - Повертає масив з інформацією про захід сонця/світанок і початок/закінчення сутінків
