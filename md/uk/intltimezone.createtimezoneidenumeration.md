---
navigation:
  - intltimezone.createtimezone.md: '« IntlTimeZone::createTimeZone'
  - intltimezone.fromdatetimezone.md: 'IntlTimeZone::fromDateTimeZone »'
  - index.md: PHP Manual
  - class.intltimezone.md: IntlTimeZone
title: 'IntlTimeZone::createTimeZoneIDEnumeration'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlTimeZone::createTimeZoneIDEnumeration

# intltz\_create\_time\_zone\_id\_enumeration

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

IntlTimeZone::createTimeZoneIDEnumeration -- intltz\_create\_time\_zone\_id\_enumeration — Отримати перерахування з ідентифікаторів системних часових поясів за умовами фільтрації

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public static IntlTimeZone::createTimeZoneIDEnumeration(int $type, ?string $region = null, ?int $rawOffset = null): IntlIterator|false
```

Процедурний стиль:

```methodsynopsis
intltz_create_time_zone_id_enumeration(int $type, ?string $region = null, ?int $rawOffset = null): IntlIterator|false
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`type`

`region`

`rawOffset`

### Значення, що повертаються

Повертає [IntlIterator](class.intliterator.md)или\*\*`false`\*\*в случае возникновения ошибки.
