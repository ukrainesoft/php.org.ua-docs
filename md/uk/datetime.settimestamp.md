---
navigation:
  - datetime.settime.md: '« DateTime::setTime'
  - datetime.settimezone.md: 'DateTime::setTimezone »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::setTimestamp'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTime::setTimestamp

# date\_timestamp\_set

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DateTime::setTimestamp -- date\_timestamp\_set — Встановлює дату та час на основі мітки часу Unix

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::setTimestamp(int $timestamp): DateTime
```

Процедурний стиль

```methodsynopsis
date_timestamp_set(DateTime $object, int $timestamp): DateTime
```

Встановлює дату та час, ґрунтуючись на мітці часу Unix.

Подобен методу[DateTimeImmutable::setTimestamp()](datetimeimmutable.settimestamp.md), крім роботи з об'єктом [DateTime](class.datetime.md)

Процедурна версія приймає об'єкт [DateTime](class.datetime.md) як перший аргумент.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [date\_create()](function.date-create.md). Функція змінює цей об'єкт.

`timestamp`

Мітка часу Unix представляє дату. Встановлення позначок часу за межами діапазону цілих чисел (int) можливе при використанні [DateTimeImmutable::modify()](datetimeimmutable.modify.md) з форматом `@`

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.md)для применения в цепи методов.

### Дивіться також

-   [DateTimeImmutable::setTimestamp()](datetimeimmutable.settimestamp.md) \- Встановлює дату та час на основі мітки часу Unix
