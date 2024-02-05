---
navigation:
  - datetimeimmutable.settime.md: '« DateTimeImmutable::setTime'
  - datetimeimmutable.settimezone.md: 'DateTimeImmutable::setTimezone »'
  - index.md: PHP Manual
  - class.datetimeimmutable.md: DateTimeImmutable
title: 'DateTimeImmutable::setTimestamp'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTimeImmutable::setTimestamp

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

DateTimeImmutable::setTimestamp — Встановлює дату та час на основі мітки часу Unix

### Опис

```methodsynopsis
public DateTimeImmutable::setTimestamp(int $timestamp): DateTimeImmutable
```

Повертає новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md), побудований зі старого, з датою та часом, встановленими на основі мітки часу Unix.

### Список параметрів

`timestamp`

Метка времени Unix, представляющая дату. Установка меток времени вне диапазона целого числа (int) возможна при использовании метода[DateTimeImmutable::modify()](datetimeimmutable.modify.md) з форматом `@`

### Значення, що повертаються

Повертає новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md) із модифікованими даними.

### Приклади

**Приклад #1 Приклад використання** DateTimeImmutable::setTimestamp()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable();
echo $date->format('U = Y-m-d H:i:s') . "\n";

$newDate = $date->setTimestamp(1171502725);
echo $newDate->format('U = Y-m-d H:i:s') . "\n";
?>
```

Висновок наведених прикладів буде схожим на:

```
1272508903 = 2010-04-28 22:41:43
1171502725 = 2007-02-14 20:25:25
```

### Дивіться також

-   [DateTimeImmutable::getTimestamp()](datetime.gettimestamp.md) \- Повертає тимчасову мітку Unix
