Повертає різницю між двома об'єктами DateTime

-   [« DateTimeInterface](class.datetimeinterface.html)
    
-   [DateTimeInterface::format »](datetime.format.html)
    
-   [PHP Manual](index.html)
    
-   [DateTimeInterface](class.datetimeinterface.html)
    
-   Повертає різницю між двома об'єктами DateTime
    

# DateTimeInterface::diff

# DateTimeImmutable::diff

# DateTime::diff

# datediff

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateTimeInterface::diff -- DateTimeImmutable::diff -- DateTime::diff -- datediff — Повертає різницю між двома об'єктами DateTime

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

Повертає різницю між двома об'єктами [DateTimeInterface](class.datetimeinterface.html)

### Список параметрів

`datetime`

Дата та час для порівняння.

`absolute`

Використовується, щоб повернути абсолютну різницю.

### Значення, що повертаються

[DateInterval](class.dateinterval.html) об'єкт представляє різницю між двома датами.

Значення, що повертається, більш конкретно представляє інтервал для застосування до вихідного об'єкта (`$this` або `$originObject`), щоб прийти до `$targetObject`. Цей процес не завжди оборотний.

### Приклади

**Приклад #1 Приклад використання **DateTimeImmutable::diff()****

Об'єктно-орієнтований стиль

```php
<?php
$origin = new DateTimeImmutable('2009-10-11');
$target = new DateTimeImmutable('2009-10-13');
$interval = $origin->diff($target);
echo $interval->format('%R%a дней');
?>
```

Процедурний стиль

```php
<?php
$origin = date_create('2009-10-11');
$target = date_create('2009-10-13');
$interval = date_diff($origin, $target);
echo $interval->format('%R%a дней');
?>
```

Результат виконання даних прикладів:

```
+2 days
```

**Приклад #2 Порівняння об'єктів [DateTime](class.datetime.html)**

> **Зауваження**
> 
> Об'єкти [DateTimeImmutable](class.datetimeimmutable.html) і [DateTime](class.datetime.html) можуть порівнюватися за допомогою [операторів порівняння](language.operators.comparison.html)

```php
<?php
$date1 = new DateTime("now");
$date2 = new DateTime("tomorrow");

var_dump($date1 == $date2);
var_dump($date1 < $date2);
var_dump($date1 > $date2);
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
bool(false)
```

### Дивіться також

-   [DateInterval::format()](dateinterval.format.html) - Форматує інтервал
-   [DateTime::add()](datetime.add.html) - Змінює об'єкт DateTime, додаючи кількість днів, місяців, років, годин, хвилин та секунд
-   [DateTime::sub()](datetime.sub.html) - Змінює вказаний об'єкт DateTime, віднімаючи вказаний об'єкт DateInterval.