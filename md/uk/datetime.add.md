---
navigation:
  - class.datetime.md: « DateTime
  - datetime.construct.md: 'DateTime::\_\_construct »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTime::add

# date\_add

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DateTime::add -- date\_add — Змінює об'єкт DateTime, додаючи кількість днів, місяців, років, годин, хвилин та секунд

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::add(DateInterval $interval): DateTime
```

Процедурний стиль

```methodsynopsis
date_add(DateTime $object, DateInterval $interval): DateTime
```

Додає заданий об'єкт [DateInterval](class.dateinterval.md) до об'єкту [DateTime](class.datetime.md)

Подобен методу[DateTimeImmutable::add()](datetimeimmutable.add.md), крім роботи з об'єктом [DateTime](class.datetime.md)

Процедурна версія приймає як перший аргумент об'єкт [DateTime](class.datetime.md)

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [date\_create()](function.date-create.md). Функція змінює цей об'єкт.

`interval`

Об'єкт класу [DateInterval](class.dateinterval.md)

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.md)для применения в цепи методов.

### Дивіться також

-   [DateTimeImmutable::add()](datetimeimmutable.add.md) \- Повертає новий об'єкт з доданою кількістю днів, місяців, років, годин, хвилин та секунд
