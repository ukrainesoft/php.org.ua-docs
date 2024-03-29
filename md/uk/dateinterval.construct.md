---
navigation:
  - class.dateinterval.md: « DateInterval
  - dateinterval.createfromdatestring.md: 'DateInterval::createFromDateString »'
  - index.md: PHP Manual
  - class.dateinterval.md: DateInterval
title: 'DateInterval::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateInterval::\_\_construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DateInterval::\_\_construct — Створює новий об'єкт DateInterval

### Опис

public **DateInterval::\_\_construct**(string`$duration`) .

Створює новий об'єкт DateInterval.

### Список параметрів

`duration`

Опис інтервалу.

Формат опису інтервалу починається з літери `P`. Кожен період інтервалу представлений цілим числом, за яким слідує покажчик його типу. Можливі типи наведено у таблиці. Якщо інтервал містить періоди, що позначають час, їх опису повинна передувати буква `T`

**Вказівники періодів `duration`**

| Указатель периода | Опис |
| --- | --- |
| `Y` | Роки |
| `M` | Місяці |
| `D` | Дні |
| `W` | Тижня. Перетворюються на дні. До PHP 8.0.0 не міг бути використаний спільно з `D` |
| `H` | годинник |
| `M` | хвилини |
| `S` | секунди |

Ось кілька простих прикладів. Два дні - `P2D`. Дві секунди `PT2S`. Шість років і п'ять хвилин `P6YT5M`

> **Зауваження** :
> 
> Покажчики повинні записуватися від більшої величини (ліворуч) до меншої величини (праворуч). Тобто, роки мають бути до місяців, місяці до днів, дні до хвилин і так далі. Таким чином, один рік і чотири дні повинні бути представлені як `P1Y4D`, але не `P4D1Y`

Задати період також можна у вигляді дати та часу. Приклад одного року та чотирьох днів може описуватися як `P0001-00-04T00:00:00`. Але значення у цьому форматі не повинні виходити за рамки допустимих значень дати та часу (наприклад, `25` годин неприпустимо)

Ці формати засновані на [» спеціфікації ISO 8601](http://en.wikipedia.org/wiki/Iso8601#Durations)

### Помилки

Когда параметр`duration` не може бути розібраний аналізатором як інтервал, викидається виняток [DateMalformedIntervalStringException](class.datemalformedintervalstringexception.md). До PHP 8.3 викидався виняток [Exception](class.exception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер замість винятку [Exception](class.exception.md) викидається виняток [DateMalformedIntervalStringException](class.datemalformedintervalstringexception.md) |
| 8.2.0 | Буде видно тільки `y`в`f` `invert`и`days`, включаючи нову логічну властивість `from_string` |
| 8.0.0 | `W` тепер може використовуватися спільно з `D` |

### Приклади

**Приклад #1 Приклад створення та використання об'єктів [DateInterval](class.dateinterval.md)**

```php
<?php
// Создание определённой даты
$someDate = \DateTime::createFromFormat("Y-m-d H:i", "2022-08-25 14:18");

// Создание интервала
$interval = new \DateInterval("P7D");

// Добавление интервала
$someDate->add($interval);

// Преобразование интервала в строку
echo $interval->format("%d");
```

Результат виконання наведеного прикладу:

**Приклад #2 Приклад использования[DateInterval](class.dateinterval.md)**

```php
<?php

$interval = new DateInterval('P1W2D');
var_dump($interval);

?>
```

Результат виконання наведеного прикладу в PHP 8.2:

```
object(DateInterval)#1 (10) {
  ["y"]=>
  int(0)
  ["m"]=>
  int(0)
  ["d"]=>
  int(9)
  ["h"]=>
  int(0)
  ["i"]=>
  int(0)
  ["s"]=>
  int(0)
  ["f"]=>
  float(0)
  ["invert"]=>
  int(0)
  ["days"]=>
  bool(false)
  ["from_string"]=>
  bool(false)
}
```

Результат виконання наведеного прикладу в PHP 8:

```
object(DateInterval)#1 (16) {
  ["y"]=>
  int(0)
  ["m"]=>
  int(0)
  ["d"]=>
  int(9)
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
  int(0)
  ["special_amount"]=>
  int(0)
  ["have_weekday_relative"]=>
  int(0)
  ["have_special_relative"]=>
  int(0)
}
```

Результат виконання наведеного прикладу в PHP 7:

```
object(DateInterval)#1 (16) {
  ["y"]=>
  int(0)
  ["m"]=>
  int(0)
  ["d"]=>
  int(2)
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
  int(0)
  ["special_amount"]=>
  int(0)
  ["have_weekday_relative"]=>
  int(0)
  ["have_special_relative"]=>
  int(0)
}
```

### Дивіться також

-   [DateInterval::format()](dateinterval.format.md) \- Форматує інтервал
-   [DateTime::add()](datetime.add.md) \- Змінює об'єкт DateTime, додаючи кількість днів, місяців, років, годин, хвилин та секунд
-   [DateTime::sub()](datetime.sub.md) \- Віднімає дні, місяці, роки, години, хвилини та секунди з об'єкта DateTime
-   [DateTime::diff()](datetime.diff.md) \- Повертає різницю між двома об'єктами DateTime
