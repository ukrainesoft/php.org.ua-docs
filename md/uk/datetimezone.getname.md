---
navigation:
  - datetimezone.getlocation.md: '« DateTimeZone::getLocation'
  - datetimezone.getoffset.md: 'DateTimeZone::getOffset »'
  - index.md: PHP Manual
  - class.datetimezone.md: DateTimeZone
title: 'DateTimeZone::getName'
---
# DateTimeZone::getName

# timezonenameget

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTimeZone::getName -- timezonenameget — Повертає ім'я часового поясу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTimeZone::getName(): string
```

Процедурний стиль

```methodsynopsis
timezone_name_get(DateTimeZone $object): string
```

Повертає ім'я часового поясу.

### Список параметрів

`object`

Об'єкт класу [DateTimeZone](class.datetimezone.md)для якого потрібно отримати ім'я.

### Значення, що повертаються

Залежно від типу зони, зсуву UTC (тип 1), абревіатури часового поясу (тип 2) та ідентифікаторів часових поясів, опублікованих у базі даних часових поясів IANA (тип 3), рядок дескриптора для створення нового об'єкта [DateTimeZone](class.datetimezone.md) з тим самим усуненням та/або правилами. Наприклад, `02:00` `CEST` або одне з імен часових поясів у [списку часових поясів](timezones.md)
