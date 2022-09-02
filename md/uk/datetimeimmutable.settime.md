---
navigation:
  - datetimeimmutable.setisodate.md: '« DateTimeImmutable::setISODate'
  - datetimeimmutable.settimestamp.md: 'DateTimeImmutable::setTimestamp »'
  - index.md: PHP Manual
  - class.datetimeimmutable.md: DateTimeImmutable
title: 'DateTimeImmutable::setTime'
---
# DateTimeImmutable::setTime

(PHP 5> = 5.5.0, PHP 7, PHP 8)

DateTimeImmutable::setTime — Встановлює час

### Опис

```methodsynopsis
public DateTimeImmutable::setTime(    int $hour,    int $minute,    int $second = 0,    int $microsecond = 0): DateTimeImmutable
```

Повертає новий об'єкт DateTimeImmutable із часом, встановленим на заданий час.

### Список параметрів

`hour`

Час часу.

`minute`

Хвилина часу.

`second`

Час секунди.

`microsecond`

Мікросекунди часу.

### Значення, що повертаються

Повертає новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md) з модифікованими даними або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Поведінка з подвоєнням існуючого годинника (під час резервного переходу на літній час) змінилася. Раніше PHP вибирав друге входження (після переходу на літній час) замість першого входження (до переходу на літній час). |
|  | Доданий параметр `microsecond` |

### Приклади

**Приклад #1 Приклад використання **DateTimeImmutable::setTime()****

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable('2001-01-01');

$newDate = $date->setTime(14, 55);
echo $date->format('Y-m-d H:i:s') . "\n";

$newDate = $date->setTime(14, 55, 24);
echo $date->format('Y-m-d H:i:s') . "\n";
?>
```

Результатом виконання даних прикладів буде щось подібне:

```
2001-01-01 14:55:00
2001-01-01 14:55:24
```

**Приклад #2 Значення, що виходять за межі діапазону, додаються до батьківських значень**

```php
<?php
$date = new DateTimeImmutable('2001-01-01');

$newDate = $date->setTime(14, 55, 24);
echo $newDate->format('Y-m-d H:i:s') . "\n";

$newDate = $date->setTime(14, 55, 65);
echo $newDate->format('Y-m-d H:i:s') . "\n";

$newDate = $date->setTime(14, 65, 24);
echo $newDate->format('Y-m-d H:i:s') . "\n";

$newDate = $date->setTime(25, 55, 24);
echo $newDate->format('Y-m-d H:i:s') . "\n";
?>
```

Результат виконання цього прикладу:

```
2001-01-01 14:55:24
2001-01-01 14:56:05
2001-01-01 15:05:24
2001-01-02 01:55:24
```

### Дивіться також

-   [DateTimeImmutable::setDate()](datetimeimmutable.setdate.md) - Встановлює дату
-   [DateTimeImmutable::setISODate()](datetimeimmutable.setisodate.md) - Встановлює дату у форматі ISO
