---
navigation:
  - datetime.setisodate.md: '« DateTime::setISODate'
  - datetime.settimestamp.md: 'DateTime::setTimestamp »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::setTime'
---
# DateTime::setTime

# datetimeset

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTime::setTime -- datetimeset - Встановлює час

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

Подібний до методу [DateTimeImmutable::setTime()](datetimeimmutable.settime.md), крім роботи з об'єктом [DateTime](class.datetime.md)

Процедурна версія приймає об'єкт [DateTime](class.datetime.md) як перший аргумент.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [datecreate()](function.date-create.md). Функція змінює цей об'єкт.

`hour`

Час нового часу.

`minute`

Хвилини нового часу.

`second`

Секунди нового часу.

`microsecond`

Мікросекунди.

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.md) для застосування в ланцюгу методів або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Поведінка з подвійним існуючим годинником (під час переходу на літній час) змінилася. Раніше PHP вибирав друге входження (після переходу на літній час), а не перше (до переходу на літній час). |
|  | Доданий параметр `microsecond` |

### Дивіться також

-   [DateTimeImmutable::setTime()](datetimeimmutable.settime.md) - Встановлює час
