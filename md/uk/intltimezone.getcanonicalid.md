---
navigation:
  - intltimezone.fromdatetimezone.md: '« IntlTimeZone::fromDateTimeZone'
  - intltimezone.getdisplayname.md: 'IntlTimeZone::getDisplayName »'
  - index.md: PHP Manual
  - class.intltimezone.md: IntlTimeZone
title: 'IntlTimeZone::getCanonicalID'
---
# IntlTimeZone::getCanonicalID

# intltzgetcanonicalід

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlTimeZone::getCanonicalID -- intltzgetcanonicalid — Отримати канонічний системний ідентифікатор часового поясу або нормалізований ідентифікатор часового поясу по заданому ідентифікатору часового поясу

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public static IntlTimeZone::getCanonicalID(string $timezoneId, bool &$isSystemId = null): string|false
```

Процедурний стиль:

```methodsynopsis
intltz_get_canonical_id(string $timezoneId, bool &$isSystemId = null): string|false
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`timezoneId`

`isSystemId`

### Значення, що повертаються
