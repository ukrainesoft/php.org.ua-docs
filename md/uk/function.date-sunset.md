---
navigation:
  - function.date-sunrise.md: « date\_sunrise
  - function.date-time-set.md: date\_time\_set »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: date\_sunset
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# date\_sunset

(PHP 5, PHP 7, PHP 8)

date\_sunset — Повертає час заходу сонця для заданого дня та місця розташування

**Увага**

Функция*ЗАСТАРІЛА*починаючи з PHP 8.1.0. Покладатися на цю функцію не рекомендується. Використовуйте замість неї функцію [date\_sun\_info()](function.date-sun-info.md)

### Опис

```methodsynopsis
date_sunset(    int $timestamp,    int $returnFormat = SUNFUNCS_RET_STRING,    ?float $latitude = null,    ?float $longitude = null,    ?float $zenith = null,    ?float $utcOffset = null): string|int|float|false
```

**date\_sunset()** повертає час заходу сонця для певних днів (заданого аргументом `timestamp`) та місця розташування.

### Список параметрів

`timestamp`

Тимчасова мітка (`timestamp`) Дня, для якого визначається час заходу сонця.

`returnFormat`

**Константи `returnFormat`**

| константа | описание | Приклад |
| --- | --- | --- |
| SUNFUNCS\_RET\_STRING | тип результату, що повертається string | 16:46 |
| SUNFUNCS\_RET\_DOUBLE | тип повертається результату float | 16.78243132 |
| SUNFUNCS\_RET\_TIMESTAMP | тип повертається результату int (тимчасова мітка) | 1095034606 |

`latitude`

За замовчуванням у Північній півкулі для Південної передається негативна величина. Дивіться також [date.default\_latitude](datetime.configuration.md#ini.date.default-latitude)

`longitude`

За замовчуванням східна для вказівки західної довготи передається негативна величина. Дивіться також [date.default\_longitude](datetime.configuration.md#ini.date.default-longitude)

`zenith`

`zenith` - це кут між центром Сонця та лінією, перпендикулярної поверхні Землі. За замовчуванням [date.sunset\_zenith](datetime.configuration.md#ini.date.sunset-zenith)

**Поширені кути `zenith`**

| Угол | Опис |
| --- | --- |
| 90°50' | Схід сонця: точка, де Сонце стає невидимим. |
| 96° | Цивільні сутінки: зазвичай використовуються для позначення кінця заходу сонця. |
| 102° | Навігаційні сутінки: точка, в якій обрій стає невидимим з моря. |
| 108° | Астрономічний сутінки: точка, в якій Сонце закінчує бути джерелом будь-якого освітлення. |

`utcOffset`

Задається в годиннику . `utcOffset` ігнорується, якщо `returnFormat` **`SUNFUNCS_RET_TIMESTAMP`**

### Значення, що повертаються

Возвращает время захода солнца в заданном формате`returnFormat`или\*\*`false`\*\* у разі виникнення помилки. Одна з можливих причин невдалого виконання – сонце не піднімається над обрієм взагалі, що відбувається всередині полярних кіл протягом частини року.

### Помилки

Кожен виклик до функцій дати/часу при неправильних налаштуваннях часового поясу згенерує помилку рівня **`E_WARNING`**, якщо часовий пояс неправильний. Дивіться також [date\_default\_timezone\_set()](function.date-default-timezone-set.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Функція оголошена застарілою, використовуйте її разом [date\_sun\_info()](function.date-sun-info.md) |
| 8.0.0 | `latitude` `longitude` `zenith`и`utcOffset` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання** date\_sunset()\*\*\*\*

```php
<?php

/* calculate the sunset time for Lisbon, Portugal
Latitude: 38.4 North
Longitude: 9 West
Zenith ~= 90
offset: +1 GMT
*/

echo date("D M d Y"). ', время захода солнца : ' .date_sunset(time(), SUNFUNCS_RET_STRING, 38.4, -9, 90, 1);

?>
```

Висновок наведеного прикладу буде схожим на:

```
Mon Dec 20 2004, время захода солнца : 18:13
```

**Приклад #2 Немає заходу сонця**

```php
<?php
$solstice = strtotime('2017-12-21');
var_dump(date_sunset($solstice, SUNFUNCS_RET_STRING, 69.245833, -53.537222));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
```

### Дивіться також

-   [date\_sun\_info()](function.date-sun-info.md) \- Повертає масив з інформацією про захід сонця/світанок і початок/закінчення сутінків
