---
navigation:
  - datetimeimmutable.set-state.html: '« DateTimeImmutable::setstate'
  - datetimeimmutable.setisodate.md: 'DateTimeImmutable::setISODate »'
  - index.md: PHP Manual
  - class.datetimeimmutable.md: DateTimeImmutable
title: 'DateTimeImmutable::setDate'
---
# DateTimeImmutable::setDate

(PHP 5> = 5.5.0, PHP 7, PHP 8)

DateTimeImmutable::setDate — Встановлює дату

### Опис

```methodsynopsis
public DateTimeImmutable::setDate(int $year, int $month, int $day): DateTimeImmutable
```

Повертає новий об'єкт DateTimeImmutable із поточною датою об'єкта DateTimeImmutable, встановленою на задану дату.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [datecreate()](function.date-create.md). Функція змінює цей об'єкт.

`year`

Рік дати.

`month`

Місяць дати.

`day`

День дати.

### Значення, що повертаються

Повертає новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md) з модифікованими даними або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **DateTimeImmutable::setDate()****

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable();
$newDate = $date->setDate(2001, 2, 3);
echo $newDate->format('Y-m-d');
?>
```

Результат виконання даних прикладів:

```
2001-02-03
```

**Приклад #2 Значення, що виходять за межі діапазону, додаються до батьківських значень**

```php
<?php
$date = new DateTimeImmutable();

$newDate = $date->setDate(2001, 2, 28);
echo $newDate->format('Y-m-d') . "\n";

$newDate = $date->setDate(2001, 2, 29);
echo $newDate->format('Y-m-d') . "\n";

$newDate = $date->setDate(2001, 14, 3);
echo $newDate->format('Y-m-d') . "\n";
?>
```

Результат виконання цього прикладу:

```
2001-02-28
2001-03-01
2002-02-03
```

### Дивіться також

-   [DateTimeImmutable::setISODate()](datetimeimmutable.setisodate.md) - Встановлює дату у форматі ISO
-   [DateTimeImmutable::setTime()](datetimeimmutable.settime.md) - Встановлює час
