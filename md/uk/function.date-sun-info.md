Повертає масив з інформацією про захід сонця/світанок і початок/закінчення сутінків

-   [« date\_sub](function.date-sub.html)
    
-   [date\_sunrise »](function.date-sunrise.html)
    
-   [PHP Manual](index.html)
    
-   [Функции даты и времени](ref.datetime.html)
    
-   Повертає масив з інформацією про захід сонця/світанок і початок/закінчення сутінків
    

# datesuninfo

(PHP 5> = 5.1.2, PHP 7, PHP 8)

datesuninfo — Повертає масив з інформацією про захід сонця/світанок і початок/закінчення сутінків

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

Повертає масив у разі успішного виконання або **`false`** у разі виникнення помилки. Структура масиву докладно описана у наступному списку:

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

Кінець навігаційного заходу (зенітний кут = 102°). Воно починається на `civil_twilight_end`

`astronomical_twilight_begin`

Початок астрономічного світанку (зенітний кут = 108 °). Воно закінчується на `nautical_twilight_begin`

`astronomical_twilight_end`

Кінець астрономічного заходу (зенітний кут = 108 °). Воно починається на `nautical_twilight_end`

Значення елементів масиву - або тимчасова мітка UNIX, **`false`**якщо сонце знаходиться нижче відповідного зеніту протягом усього дня, або **`true`**якщо сонце знаходиться вище відповідного зеніту протягом усього дня.

### список змін

| Версия | Описание                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------|
|        | Розрахунок був виправлений з урахуванням місцевої опівночі замість місцевого полудня, що дещо змінює результати. |

### Приклади

**Приклад #1 Приклад використання **datesuninfo()****

```php
<?php
$sun_info = date_sun_info(strtotime("2006-12-12"), 31.7667, 35.2333);
foreach ($sun_info as $key => $val) {
    echo "$key: " . date("H:i:s", $val) . "\n";
}
?>
```

Результат виконання цього прикладу:

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

**Приклад #2 Полярна ніч**

```php
<?php
var_dump(date_sun_info(strtotime("2017-12-21"), 90, 0));
?>
```

Результат виконання цього прикладу:

```
array(9) {
  ["sunrise"]=>
  bool(false)
  ["sunset"]=>
  bool(false)
  ["transit"]=>
  int(1513857490)
  ["civil_twilight_begin"]=>
  bool(false)
  ["civil_twilight_end"]=>
  bool(false)
  ["nautical_twilight_begin"]=>
  bool(false)
  ["nautical_twilight_end"]=>
  bool(false)
  ["astronomical_twilight_begin"]=>
  bool(false)
  ["astronomical_twilight_end"]=>
  bool(false)
}
```

**Приклад #3 Опівнічне сонце**

```php
<?php
var_dump(date_sun_info(strtotime("2017-06-21"), 90, 0));
?>
```

Результат виконання цього прикладу:

```
array(9) {
  ["sunrise"]=>
  bool(true)
  ["sunset"]=>
  bool(true)
  ["transit"]=>
  int(1498046510)
  ["civil_twilight_begin"]=>
  bool(true)
  ["civil_twilight_end"]=>
  bool(true)
  ["nautical_twilight_begin"]=>
  bool(true)
  ["nautical_twilight_end"]=>
  bool(true)
  ["astronomical_twilight_begin"]=>
  bool(true)
  ["astronomical_twilight_end"]=>
  bool(true)
}
```

### Дивіться також

-   [date\_sunrise()](function.date-sunrise.html) - Повертає час світанку для заданого дня та місця розташування
-   [date\_sunset()](function.date-sunset.html) - Повертає час заходу сонця для заданого дня та місця розташування