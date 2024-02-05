---
navigation:
  - intltimezone.getunknown.md: '« IntlTimeZone::getUnknown'
  - intltimezone.hassamerules.md: 'IntlTimeZone::hasSameRules »'
  - index.md: PHP Manual
  - class.intltimezone.md: IntlTimeZone
title: 'IntlTimeZone::getWindowsID'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlTimeZone::getWindowsID

# intltz\_get\_windows\_id

(PHP 7 >= 7.1.0, PHP 8)

IntlTimeZone::getWindowsID -- intltz\_get\_windows\_id — Перетворити часовий пояс на часовий пояс для Windows

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public static IntlTimeZone::getWindowsID(string $timezoneId): string|false
```

Процедурний стиль:

```methodsynopsis
intltz_get_windows_id(string $timezoneId): string|false
```

Переводить системний часовий пояс (наприклад, «America/Los\_Angeles») у часовий пояс для Windows (наприклад, «Pacific Standard Time»).

> **Зауваження**: Ця функція потребує ICU версії ≥ 52.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`timezoneId`

### Значення, що повертаються

Повертає часовий пояс для Windows або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [IntlTimeZone::getIDForWindowsID()](intltimezone.getidforwindowsid.md) \- Перетворити часовий пояс для Windows на системний часовий пояс
