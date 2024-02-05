---
navigation:
  - dateinterval.construct.md: '« DateInterval::\_\_construct'
  - dateinterval.format.md: 'DateInterval::format »'
  - index.md: PHP Manual
  - class.dateinterval.md: DateInterval
title: 'DateInterval::createFromDateString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateInterval::createFromDateString

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DateInterval::createFromDateString — Створює об'єкт класу DateInterval із дати у відносному форматі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static DateInterval::createFromDateString(string $datetime): DateInterval|false
```

Процедурний стиль

```methodsynopsis
date_interval_create_from_date_string(string $datetime): DateInterval|false
```

Використовує парсер дати/часу, який використовується в конструкторі [DateTimeImmutable](class.datetimeimmutable.md) для створення об'єкта [DateInterval](class.dateinterval.md) із відносних частин розібраного рядка.

### Список параметрів

`datetime`

Дата, що складається з відносних часових фрагментів. Зокрема, для створення об'єкта DateInterval із частин, записаних у відносному форматі, який підтримується парсером у функціях [DateTimeImmutable](class.datetimeimmutable.md) [DateTime](class.datetime.md) і [strtotime()](function.strtotime.md)

Щоб використовувати рядок у форматі ISO-8601, наприклад `P7D`необхідно використовувати конструктор.

### Значення, що повертаються

Повертає новий об'єкт класу [DateInterval](class.dateinterval.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тільки властивості `from_string`и`date_string` буде видно при створенні об'єкта [DateInterval](class.dateinterval.md) за допомогою цього. |

### Приклади

**Приклад #1 Аналіз та розбір часових інтервалів**

```php
<?php
// Интервалы в каждом Прикладе эквивалентны.
$i = new DateInterval('P1D');
$i = DateInterval::createFromDateString('1 day');

$i = new DateInterval('P2W');
$i = DateInterval::createFromDateString('2 weeks');

$i = new DateInterval('P3M');
$i = DateInterval::createFromDateString('3 months');

$i = new DateInterval('P4Y');
$i = DateInterval::createFromDateString('4 years');

$i = new DateInterval('P1Y1D');
$i = DateInterval::createFromDateString('1 year + 1 day');

$i = new DateInterval('P1DT12H');
$i = DateInterval::createFromDateString('1 day + 12 hours');

$i = new DateInterval('PT3600S');
$i = DateInterval::createFromDateString('3600 seconds');
?>
```

**Приклад #2 Розбір комбінацій та негативних інтервалів**

```php
<?php
$i = DateInterval::createFromDateString('62 weeks + 1 day + 2 weeks + 2 hours + 70 minutes');
echo $i->format('%d %h %i'), "\n";

$i = DateInterval::createFromDateString('1 year - 10 days');
echo $i->format('%y %d'), "\n";
?>
```

Результат виконання наведеного прикладу:

449 2 70

**Приклад #3 Розбір спеціальних відносних часових інтервалів**

```php
<?php
$i = DateInterval::createFromDateString('last day of next month');
var_dump($i);

$i = DateInterval::createFromDateString('last weekday');
var_dump($i);
```

Результат виконання наведеного прикладу в PHP 8.2:

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

Результат виконання наведеного прикладу PHP 8 аналогічний:

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
