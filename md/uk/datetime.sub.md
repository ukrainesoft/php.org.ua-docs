---
navigation:
  - datetime.settimezone.md: '« DateTime::setTimezone'
  - class.datetimeimmutable.md: DateTimeImmutable »
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::sub'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTime::sub

# date\_sub

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DateTime::sub -- date\_sub — Віднімає дні, місяці, роки, години, хвилини та секунди з об'єкта DateTime

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::sub(DateInterval $interval): DateTime
```

Процедурний стиль

```methodsynopsis
date_sub(DateTime $object, DateInterval $interval): DateTime
```

Віднімає з часу об'єкта DateTime заданий інтервал [DateInterval](class.dateinterval.md)

Подобен методу[DateTimeImmutable::sub()](datetimeimmutable.sub.md), крім роботи з об'єктом [DateTime](class.datetime.md)

Процедурна версія приймає об'єкт [DateTime](class.datetime.md) як перший аргумент.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [date\_create()](function.date-create.md). Функція змінює цей об'єкт.

`interval`

Об'єкт класу [DateInterval](class.dateinterval.md)

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.md)для применения в цепи методов.

### Помилки

Лише об'єкт-орієнтований API: При спробі виконати непідтримувану операцію, наприклад, якщо в об'єкті [DateInterval](class.dateinterval.md) містяться відносні характеристики часу (наприклад, `next weekday`), буде викинуто виняток [DateInvalidOperationException](class.dateinvalidoperationexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер замість попередження у методі **DateTime::sub()** викидається виняток [DateInvalidOperationException](class.dateinvalidoperationexception.md), якщо була спроба виконати непідтримувану операцію. Функція [date\_sub()](function.date-sub.md) не було змінено. |

### Дивіться також

-   [DateTimeImmutable::sub()](datetimeimmutable.sub.md) \- Віднімає передану кількість днів, місяців, років, годин, хвилин та секунд
