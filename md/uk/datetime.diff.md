---
navigation:
  - class.datetimeinterface.md: « DateTimeInterface
  - datetime.format.md: 'DateTimeInterface::format »'
  - index.md: PHP Manual
  - class.datetimeinterface.md: DateTimeInterface
title: 'DateTimeInterface::diff'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTimeInterface::diff

# DateTimeImmutable::diff

# DateTime::diff

# date\_diff

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DateTimeInterface::diff -- DateTimeImmutable::diff -- DateTime::diff -- date\_diff — Повертає різницю між двома об'єктами DateTime

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTimeInterface::diff(DateTimeInterface $targetObject, bool $absolute = false): DateInterval
```

```methodsynopsis
public DateTimeImmutable::diff(DateTimeInterface $targetObject, bool $absolute = false): DateInterval
```

```methodsynopsis
public DateTime::diff(DateTimeInterface $targetObject, bool $absolute = false): DateInterval
```

Процедурний стиль

```methodsynopsis
date_diff(DateTimeInterface $baseObject, DateTimeInterface $targetObject, bool $absolute = false): DateInterval
```

Повертає різницю між двома об'єктами [DateTimeInterface](class.datetimeinterface.md)

### Список параметрів

`datetime`

Дата та час для порівняння.

`absolute`

Визначає, чи інтервал примусово переведений в абсолютну величину.

### Значення, що повертаються

Повертає об'єкт [DateInterval](class.dateinterval.md)який представляє різницю між двома датами.

Значення, що повертається, більш конкретно представляє часовий інтервал, який при застосуванні до вихідного об'єкта (`$this`или`$originObject`) призводить до об'єкту `$targetObject`. Цей процес не завжди оборотний.

Метод враховує зміну часових поясів і тому може повертати інтервал `24 hours and 30 minutes`, як у одному з прикладів. Якщо потрібно розраховувати за абсолютним часом, необхідно спочатку перетворити об'єкти `$this` `$baseObject`и`$targetObject`в UTC.

### Приклади

**Приклад #1 Приклад использования метода**DateTimeInterface::diff()\*\* з діапазоном дат\*\*

Значення, яке повертає метод, - це точна кількість часу, яка необхідна для переходу від часу об'єкта `$this` на час об'єкта `$targetObject`. Тому порівняння 1 січня із 31 грудня повертає 364 дні, а не 365 днів (для невисокосних років).

```php
<?php
$originalTime = new DateTimeImmutable("2023-01-01 UTC");
$targedTime = new DateTimeImmutable("2023-12-31 UTC");
$interval = $originalTime->diff($targedTime);
echo "Полных дней: ", $interval->format("%a"), "\n";
?>
```

Результат виконання наведеного прикладу:

```
Полных дней: 364
```

**Приклад #2 Приклад використання** DateTimeImmutable::diff()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
$origin = new DateTimeImmutable('2009-10-11');
$target = new DateTimeImmutable('2009-10-13');
$interval = $origin->diff($target);
echo $interval->format('%R%a дней');
?>
```

Процедурний стиль

```php
<?php
$origin = date_create('2009-10-11');
$target = date_create('2009-10-13');
$interval = date_diff($origin, $target);
echo $interval->format('%R%a дней');
?>
```

Результат виконання наведених прикладів:

```
+2 days
```

**Приклад #3 Приклад використання** DateTimeInterface::diff()**во время перехода на летнее время**

```php
<?php
$originalTime = new DateTimeImmutable("2021-10-30 09:00:00 Europe/London");
$targedTime = new DateTimeImmutable("2021-10-31 08:30:00 Europe/London");
$interval = $originalTime->diff($targedTime);
echo $interval->format("%H:%I:%S (Полных дней: %a)"), "\n";
?>
```

Результат виконання наведеного прикладу:

```
24:30:00 (Полных дней: 0)
```

**Приклад #4 Порівняння об'єктів [DateTime](class.datetime.md)**

> **Зауваження** :
> 
> Об'єкти [DateTimeImmutable](class.datetimeimmutable.md) і [DateTime](class.datetime.md) можна порівнювати [операторами порівняння](language.operators.comparison.md)

```php
<?php
$date1 = new DateTime("now");
$date2 = new DateTime("tomorrow");

var_dump($date1 == $date2);
var_dump($date1 < $date2);
var_dump($date1 > $date2);
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
bool(false)
```

### Дивіться також

-   [DateInterval::format()](dateinterval.format.md) \- Форматує інтервал
-   [DateTime::add()](datetime.add.md) \- Змінює об'єкт DateTime, додаючи кількість днів, місяців, років, годин, хвилин та секунд
-   [DateTime::sub()](datetime.sub.md) \- Віднімає дні, місяці, роки, години, хвилини та секунди з об'єкта DateTime
