---
navigation:
  - datetime.setisodate.md: '« DateTime::setISODate'
  - datetime.settimestamp.md: 'DateTime::setTimestamp »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::setTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTime::setTime

# date\_time\_set

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

DateTime::setTime -- date\_time\_set - Встановлює час

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::setTime(    int $hour,    int $minute,    int $second = 0,    int $microsecond = 0): DateTime
```

Процедурний стиль

```methodsynopsis
date_time_set(    DateTime $object,    int $hour,    int $minute,    int $second = 0,    int $microsecond = 0): DateTime
```

Встановлює поточне значення часу об'єкта DateTime на нове значення.

Подобен методу[DateTimeImmutable::setTime()](datetimeimmutable.settime.md), крім роботи з об'єктом [DateTime](class.datetime.md)

Процедурна версія приймає об'єкт [DateTime](class.datetime.md) як перший аргумент.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [date\_create()](function.date-create.md). Функція змінює цей об'єкт.

`hour`

Час нового часу.

`minute`

Хвилини нового часу.

`second`

Секунди нового часу.

`microsecond`

Мікросекунди.

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.md)для применения в цепи методов.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Поведінка з подвійним існуючим годинником (під час переходу на літній час) змінилася. Раніше PHP вибирав друге входження (після переходу на літній час), а не перше (до переходу на літній час). |
| 7.1.0 | Добавлен параметр`microsecond` |

### Дивіться також

-   [DateTimeImmutable::setTime()](datetimeimmutable.settime.md) \- Встановлює час
