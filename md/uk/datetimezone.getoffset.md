Повертає усунення часового поясу від UTC (GMT)

-   [« DateTimeZone::getName](datetimezone.getname.html)
    
-   [DateTimeZone::getTransitions »](datetimezone.gettransitions.html)
    
-   [PHP Manual](index.html)
    
-   [DateTimeZone](class.datetimezone.html)
    
-   Повертає усунення часового поясу від UTC (GMT)
    

# DateTimeZone::getOffset

# timezoneoffsetget

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTimeZone::getOffset -- timezoneoffsetget — Повертає зсув часового поясу від UTC (GMT)

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTimeZone::getOffset(DateTimeInterface $datetime): int
```

Процедурний стиль

```methodsynopsis
timezone_offset_get(DateTimeZone $object, DateTimeInterface $datetime): int
```

Ця функція повертає зсув від GMT для дати/часу, зазначених у параметрі `datetime`. GMT-зміщення розраховується за допомогою інформації про часовий пояс, що міститься у об'єкті DateTimeZone, що використовується.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTimeZone](class.datetimezone.html), що повертається [timezoneopen()](function.timezone-open.html)

`datetime`

DateTime, що містить дату/час, щодо яких обчислюється зміщення.

### Значення, що повертаються

Повертає зміщення часового поясу за секунди.

### список змін

| Версия | Описание |
| --- | --- |
|  | До цієї версії, у разі виникнення помилки поверталося **`false`** |

### Приклади

**Приклад #1 Приклад використання **DateTimeZone::getOffset()****

```php
<?php
// Создание двух объектов timezone, один для Тайбэй (Тайвань) и один для
// Токио (Япония)
$dateTimeZoneTaipei = new DateTimeZone("Asia/Taipei");
$dateTimeZoneJapan = new DateTimeZone("Asia/Tokyo");

// Создание двух объектов DateTime, которые будут содержать одинаковые метки времени Unix, но
// имеющих различные часовые пояса.
$dateTimeTaipei = new DateTime("now", $dateTimeZoneTaipei);
$dateTimeJapan = new DateTime("now", $dateTimeZoneJapan);

// Вычисление смещения от GMT для даты/времени, содержащихся в объекте $dateTimeTaipei,
// но с использованием правил часового пояса, определённых для Токио
// ($dateTimeZoneJapan).
$timeOffset = $dateTimeZoneJapan->getOffset($dateTimeTaipei);

// Должен показать int(32400) (для дат после Sat Sep 8 01:00:00 1951 JST).
var_dump($timeOffset);
?>
```