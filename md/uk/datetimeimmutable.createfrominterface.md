---
navigation:
  - datetimeimmutable.createfromformat.md: '« DateTimeImmutable::createFromFormat'
  - datetimeimmutable.createfrommutable.md: 'DateTimeImmutable::createFromMutable »'
  - index.md: PHP Manual
  - class.datetimeimmutable.md: DateTimeImmutable
title: 'DateTimeImmutable::createFromInterface'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTimeImmutable::createFromInterface

(PHP 8)

DateTimeImmutable::createFromInterface — Повертає новий об'єкт DateTimeImmutable, створений з переданого об'єкта, що реалізує інтерфейс DateTimeInterface

### Опис

```methodsynopsis
public static DateTimeImmutable::createFromInterface(DateTimeInterface $object): DateTimeImmutable
```

### Список параметрів

`object`

Об'єкт, що реалізує інтерфейс [DateTimeInterface](class.datetimeinterface.md), який необхідно сконвертувати на іммутабельну версію. Сам об'єкт не змінюється. Натомість повертається новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md) з тими самими значеннями дати, часу та часового поясу.

### Значення, що повертаються

Повертає новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md)

### Приклади

**Приклад #1 Створення іммутабельного об'єкта дати та часу**

```php
<?php
$date = new DateTime("2014-06-20 11:45 Europe/London");

$immutable = DateTimeImmutable::createFromInterface($date);

$date = new DateTimeImmutable("2014-06-20 11:45 Europe/London");
$also_immutable = DateTimeImmutable::createFromInterface($date);
?>
```
