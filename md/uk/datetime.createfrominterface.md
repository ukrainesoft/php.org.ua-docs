---
navigation:
  - datetime.createfromimmutable.md: '« DateTime::createFromImmutable'
  - datetime.getlasterrors.md: 'DateTime::getLastErrors »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::createFromInterface'
---
# DateTime::createFromInterface

(PHP 8)

DateTime::createFromInterface - Повертає новий об'єкт DateTime, створений з переданого об'єкта, що реалізує інтерфейс DateTimeInterface

### Опис

```methodsynopsis
public static DateTime::createFromInterface(DateTimeInterface $object): DateTime
```

### Список параметрів

`object`

Об'єкт, що реалізує інтерфейс [DateTimeInterface](class.datetimeinterface.md), з якого треба отримати версію, що змінюється. Сам об'єкт не модифікується. На його основі створюється новий об'єкт [DateTime](class.datetime.md), що містить ту ж інформацію про дату, час і часовий пояс.

### Значення, що повертаються

Повертає новий об'єкт [DateTime](class.datetime.md)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$date = new DateTimeImmutable("2014-06-20 11:45 Europe/London");

$mutable = DateTime::createFromInterface($date);

$date = new DateTime("2014-06-20 11:45 Europe/London");
$also_mutable = DateTime::createFromInterface($date);
?>
```
