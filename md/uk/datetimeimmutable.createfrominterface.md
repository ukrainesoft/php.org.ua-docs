Повертає новий об'єкт DateTimeImmutable, створений із переданого об'єкта, що реалізує інтерфейс DateTimeInterface

-   [« DateTimeImmutable::createFromFormat](datetimeimmutable.createfromformat.html)
    
-   [DateTimeImmutable::createFromMutable »](datetimeimmutable.createfrommutable.html)
    
-   [PHP Manual](index.html)
    
-   [DateTimeImmutable](class.datetimeimmutable.html)
    
-   Повертає новий об'єкт DateTimeImmutable, створений із переданого об'єкта, що реалізує інтерфейс DateTimeInterface
    

# DateTimeImmutable::createFromInterface

(PHP 8)

DateTimeImmutable::createFromInterface — Повертає новий об'єкт DateTimeImmutable, створений з переданого об'єкта, що реалізує інтерфейс DateTimeInterface

### Опис

```methodsynopsis
public static DateTimeImmutable::createFromInterface(DateTimeInterface $object): DateTimeImmutable
```

### Список параметрів

`object`

Об'єкт, що реалізує інтерфейс [DateTimeInterface](class.datetimeinterface.html), який необхідно конвертувати на іммутабельну версію. Сам об'єкт не змінюється. Натомість повертається новий об'єкт [DateTimeImmutable](class.datetimeimmutable.html) з тими самими значеннями дати, часу та часового поясу.

### Значення, що повертаються

Повертає новий об'єкт [DateTimeImmutable](class.datetimeimmutable.html)

### Приклади

**Приклад #1 Створення іммутабельного об'єкта дати та часу**

```php
<?php
$date = new DateTime("2014-06-20 11:45 Europe/London");

$immutable = DateTimeImmutable::createFromInterface($date);

$date = new DateTimeImmutable("2014-06-20 11:45 Europe/London");
$also_immutable = DateTimeImmutable::createFromInterface($date);
?>
```