---
navigation:
  - intltimezone.getrawoffset.md: '« IntlTimeZone::getRawOffset'
  - intltimezone.gettzdataversion.md: 'IntlTimeZone::getTZDataVersion »'
  - index.md: PHP Manual
  - class.intltimezone.md: IntlTimeZone
title: 'IntlTimeZone::getRegion'
---
# IntlTimeZone::getRegion

# intltzgetregion

(PHP 5> = 5.5.0, PHP 7, PHP 8)

IntlTimeZone::getRegion -- intltzgetregion — Отримати код регіону, який відповідає заданому ідентифікатору системного часового поясу

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public static IntlTimeZone::getRegion(string $timezoneId): string|false
```

Процедурний стиль:

```methodsynopsis
intltz_get_region(string $timezoneId): string|false
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`timezoneId`

### Значення, що повертаються

Повертає регіон або **`false`** у разі виникнення помилки.
