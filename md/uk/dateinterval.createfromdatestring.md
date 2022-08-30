Створює об'єкт класу DateInterval із дати у відносному форматі

-   [« DateInterval::construct](dateinterval.construct.html)
    
-   [DateInterval::format »](dateinterval.format.html)
    
-   [PHP Manual](index.html)
    
-   [DateInterval](class.dateinterval.html)
    
-   Створює об'єкт класу DateInterval із дати у відносному форматі
    

# DateInterval::createFromDateString

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateInterval::createFromDateString — Створює об'єкт класу DateInterval із дати у відносному форматі

### Опис

```methodsynopsis
public static DateInterval::createFromDateString(string $datetime): DateInterval|false
```

Розбирає рядок, що містить часовий інтервал у звичайному (здобутаному) вигляді і створює на його основі об'єкт класу DateInterval.

### Список параметрів

`datetime`

Дата, що складається з відносних часових фрагментів. Зокрема, для створення об'єкта DateInterval із частин, записаних у [відносному форматі](datetime.formats.relative.html), який підтримується парсером у функціях [DateTimeImmutable](class.datetimeimmutable.html) [DateTime](class.datetime.html) і [strtotime()](function.strtotime.html)

### Значення, що повертаються

Повертає новий об'єкт класу [DateInterval](class.dateinterval.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тільки властивості `from_string` і `date_string` буде видно при створенні об'єкта [DateInterval](class.dateinterval.html) за допомогою цього. |

### Приклади

**Приклад #1 Аналіз та розбір часових інтервалів**

```php
<?php
// Интервалы в каждом примере эквивалентны.
$i = new DateInterval('P1D');
$i = DateInterval::createFromDateString('1 day');

$i = new DateInterval('P2W');
$i = DateInterval::createFromDateString('2 weeks');

$i = new DateInterval('P3M');
$i = DateInterval::createFromDateString('3 months');

$i = new DateInterval('P4Y');
$i = DateInterval::createFromDateString('4 years');

$i = new DateInterval('P1Y1D');
$i = DateInterval::createFromDateString('1 year + 1 day');

$i = new DateInterval('P1DT12H');
$i = DateInterval::createFromDateString('1 day + 12 hours');

$i = new DateInterval('PT3600S');
$i = DateInterval::createFromDateString('3600 seconds');
?>
```

**Приклад #2 Розбір спеціальних відносних часових інтервалів**

```php
<?php
$i = DateInterval::createFromDateString('last day of next month');
var_dump($i);

$i = DateInterval::createFromDateString('last weekday');
var_dump($i);
```

Результат виконання цього прикладу в PHP 8.2:

```
object(DateInterval)#1 (2) {
  ["from_string"]=>
  bool(true)
  ["date_string"]=>
  string(22) "last day of next month"
}
object(DateInterval)#2 (2) {
  ["from_string"]=>
  bool(true)
  ["date_string"]=>
  string(12) "last weekday"
}
```

Результат виконання цього прикладу в PHP 8 аналогічний:

```
object(DateInterval)#1 (16) {
  ["y"]=>
  int(0)
  ["m"]=>
  int(1)
  ["d"]=>
  int(0)
  ["h"]=>
  int(0)
  ["i"]=>
  int(0)
  ["s"]=>
  int(0)
  ["f"]=>
  float(0)
  ["weekday"]=>
  int(0)
  ["weekday_behavior"]=>
  int(0)
  ["first_last_day_of"]=>
  int(2)
  ["invert"]=>
  int(0)
  ["days"]=>
  bool(false)
  ["special_type"]=>
  int(0)
  ["special_amount"]=>
  int(0)
  ["have_weekday_relative"]=>
  int(0)
  ["have_special_relative"]=>
  int(0)
}
object(DateInterval)#2 (16) {
  ["y"]=>
  int(0)
  ["m"]=>
  int(0)
  ["d"]=>
  int(0)
  ["h"]=>
  int(0)
  ["i"]=>
  int(0)
  ["s"]=>
  int(0)
  ["f"]=>
  float(0)
  ["weekday"]=>
  int(0)
  ["weekday_behavior"]=>
  int(0)
  ["first_last_day_of"]=>
  int(0)
  ["invert"]=>
  int(0)
  ["days"]=>
  bool(false)
  ["special_type"]=>
  int(1)
  ["special_amount"]=>
  int(-1)
  ["have_weekday_relative"]=>
  int(0)
  ["have_special_relative"]=>
  int(1)
}
```