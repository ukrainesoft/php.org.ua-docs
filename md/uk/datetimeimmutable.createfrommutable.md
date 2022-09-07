---
navigation:
  - datetimeimmutable.createfrominterface.md: '« DateTimeImmutable::createFromInterface'
  - datetimeimmutable.getlasterrors.md: 'DateTimeImmutable::getLastErrors »'
  - index.md: PHP Manual
  - class.datetimeimmutable.md: DateTimeImmutable
title: 'DateTimeImmutable::createFromMutable'
---
# DateTimeImmutable::createFromMutable

(PHP 5> = 5.6.0, PHP 7, PHP 8)

DateTimeImmutable::createFromMutable — Повертає новий об'єкт DateTimeImmutable, що містить заданий об'єкт DateTime

### Опис

```methodsynopsis
public static DateTimeImmutable::createFromMutable(DateTime $object): DateTimeImmutable
```

### Список параметрів

`object`

Об'єкт, що змінюється [DateTime](class.datetime.md), який ви хочете перетворити на незмінну версію. Цей об'єкт не змінюється, але натомість створюється новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md), що містить ту саму інформацію.

### Значення, що повертаються

Повертає новий екземпляр [DateTimeImmutable](class.datetimeimmutable.md)

### Приклади

**Приклад #1 Створення незмінного об'єкта дати/часу**

```php
<?php
$date = new DateTime("2014-06-20 11:45 Europe/London");

$immutable = DateTimeImmutable::createFromMutable( $date );
?>
```
