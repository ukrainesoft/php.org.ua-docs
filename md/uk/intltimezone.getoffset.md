---
navigation:
  - intltimezone.getidforwindowsid.md: '« IntlTimeZone::getIDForWindowsID'
  - intltimezone.getrawoffset.md: 'IntlTimeZone::getRawOffset »'
  - index.md: PHP Manual
  - class.intltimezone.md: IntlTimeZone
title: 'IntlTimeZone::getOffset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlTimeZone::getOffset

# intltz\_get\_offset

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlTimeZone::getOffset -- intltz\_get\_offset — Отримати необроблене значення часового поясу та усунення за Гринвічем (GMT) за заданим моментом часу

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public IntlTimeZone::getOffset(    float $timestamp,    bool $local,    int &$rawOffset,    int &$dstOffset): bool
```

Процедурний стиль:

```methodsynopsis
intltz_get_offset(    IntlTimeZone $timezone,    float $timestamp,    bool $local,    int &$rawOffset,    int &$dstOffset): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`timestamp`

`local`

`rawOffset`

`dstOffset`

### Значення, що повертаються
