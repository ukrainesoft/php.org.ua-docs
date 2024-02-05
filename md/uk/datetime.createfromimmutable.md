---
navigation:
  - datetime.createfromformat.md: '« DateTime::createFromFormat'
  - datetime.createfrominterface.md: 'DateTime::createFromInterface »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::createFromImmutable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTime::createFromImmutable

(PHP 7 >= 7.3.0, PHP 8)

DateTime::createFromImmutable — Повертає екземпляр DateTime інкапсулюючий заданий об'єкт DateTimeImmutable

### Опис

```methodsynopsis
public static DateTime::createFromImmutable(DateTimeImmutable $object): static
```

### Список параметрів

`object`

Незмінний об'єкт [DateTimeImmutable](class.datetimeimmutable.md), який потребує перетворення на змінну форму. Сам об'єкт не змінюється, а натомість створюється новий екземпляр [DateTime](class.datetime.md), що містить самі дані: дату, час і часовий пояс.

### Значення, що повертаються

Повертає новий об'єкт класу [DateTime](class.datetime.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод тепер повертає екземпляр поточного класу, що викликається; раніше він створював новий екземпляр класу [DateTime](class.datetime.md) |

### Приклади

**Приклад #1 Створення об'єкта, що змінюється**

```php
<?php
$date = new DateTimeImmutable("2014-06-20 11:45 Europe/London");

$mutable = DateTime::createFromImmutable( $date );
?>
```
