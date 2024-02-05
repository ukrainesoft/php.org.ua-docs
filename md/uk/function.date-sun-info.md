---
navigation:
  - function.date-sub.md: « date\_sub
  - function.date-sunrise.md: date\_sunrise »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: date\_sun\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# date\_sun\_info

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

date\_sun\_info — Повертає масив з інформацією про захід сонця/світанок і початок/закінчення сутінків

### Опис

```methodsynopsis
date_sun_info(int $timestamp, float $latitude, float $longitude): array
```

### Список параметрів

`timestamp`

Тимчасова мітка Unix.

`latitude`

Широта у градусах.

`longitude`

Довгота у градусах.

### Значення, що повертаються

Повертає масив у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Структура массива подробно описана в следующем списке:

`sunrise`

Тимчасова мітка сходу сонця (зенітний кут = 90 ° 35 ').

`sunset`

Тимчасова мітка заходу сонця (зенітний кут = 90 ° 35 ').

`transit`

Тимчасова мітка, коли сонце знаходиться у своєму зеніті, тобто досягло найвищої точки.

`civil_twilight_begin`

Початок громадянського світанку (зенітний кут = 96 °). Воно закінчується на `sunrise`

`civil_twilight_end`

Кінець громадянського заходу сонця (зенітний кут = 96°). Воно починається на `sunset`

`nautical_twilight_begin`

Початок навігаційного світанку (зенітний кут = 102 °). Воно закінчується `civil_twilight_begin`

`nautical_twilight_end`

Кінець навігаційного заходу (зенітний кут = 102 °). Воно починається на `civil_twilight_end`

`astronomical_twilight_begin`

Початок астрономічного світанку (зенітний кут = 108 °). Воно закінчується на `nautical_twilight_begin`

`astronomical_twilight_end`

Кінець астрономічного заходу сонця (зенітний кут = 108°). Воно починається на `nautical_twilight_end`

Значення елементів масиву - або тимчасова мітка UNIX, \*\*`false`\*\*якщо сонце знаходиться нижче відповідного зеніту протягом усього дня, або \*\*`true`\*\*якщо сонце знаходиться вище відповідного зеніту протягом усього дня.

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Розрахунок був виправлений з урахуванням місцевої опівночі замість місцевого полудня, що дещо змінює результати. |

### Приклади

**Приклад #1 Приклад використання** date\_sun\_info()\*\*\*\*

```php
<?php
$sun_info = date_sun_info(strtotime("2006-12-12"), 31.7667, 35.2333);
foreach ($sun_info as $key => $val) {
    echo "$key: " . date("H:i:s", $val) . "\n";
}
?>
```

Результат виконання наведеного прикладу:

```
sunrise: 05:52:11
sunset: 15:41:21
transit: 10:46:46
civil_twilight_begin: 05:24:08
civil_twilight_end: 16:09:24
nautical_twilight_begin: 04:52:25
nautical_twilight_end: 16:41:06
astronomical_twilight_begin: 04:21:32
astronomical_twilight_end: 17:12:00
```

**Приклад #2 Полярна ніч із деякою обробкою**

```php
<?php
$tz = new \DateTimeZone('America/Anchorage');
$si = date_sun_info(strtotime("2022-12-21"), 70.21, -148.51);
foreach ($si as $key => $value) {
    echo
        match ($value) {
            true => 'always',
            false => 'never',
            default => date_create("@{$value}")->setTimeZone($tz)->format( 'H:i:s T' ),
        },
        ": {$key}",
        "\n";
}?>
```

Результат виконання наведеного прикладу:

```
never: sunrise
never: sunset
12:52:18 AKST: transit
10:53:19 AKST: civil_twilight_begin
14:51:17 AKST: civil_twilight_end
09:01:47 AKST: nautical_twilight_begin
16:42:48 AKST: nautical_twilight_end
07:40:47 AKST: astronomical_twilight_begin
18:03:49 AKST: astronomical_twilight_end
```

**Приклад #3 Опівнічне сонце (Тромсе, Норвегія)**

```php
<?php
$si = date_sun_info(strtotime("2022-06-26"), 69.68, 18.94);
print_r($si);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [sunrise] => 1
    [sunset] => 1
    [transit] => 1656240426
    [civil_twilight_begin] => 1
    [civil_twilight_end] => 1
    [nautical_twilight_begin] => 1
    [nautical_twilight_end] => 1
    [astronomical_twilight_begin] => 1
    [astronomical_twilight_end] => 1
)
```

**Приклад #4 Обчислення тривалості дня (Київ)**

```php
<?php
$si = date_sun_info(strtotime('2022-08-26'), 50.45, 30.52);
$diff = $si['sunset'] - $si['sunrise'];
echo "Продолжительность дня: ",
    floor($diff / 3600), " ч. ",
    floor(($diff % 3600) / 60), " сек.\n";
?>
```

Результат виконання наведеного прикладу:

```
Продолжительность дня: 13 ч. 56 сек.
```

### Дивіться також

-   [date\_sunrise()](function.date-sunrise.md) \- Повертає час світанку для заданого дня та місця розташування
-   [date\_sunset()](function.date-sunset.md) \- Повертає час заходу сонця для заданого дня та місця розташування
