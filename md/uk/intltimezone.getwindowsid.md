---
navigation:
  - intltimezone.getunknown.html: '« IntlTimeZone::getUnknown'
  - intltimezone.hassamerules.html: 'IntlTimeZone::hasSameRules »'
  - index.html: PHP Manual
  - class.intltimezone.html: IntlTimeZone
title: 'IntlTimeZone::getWindowsID'
---
# IntlTimeZone::getWindowsID

# intltzgetwindowsід

(PHP 7> = 7.1.0, PHP 8)

IntlTimeZone::getWindowsID -- intltzgetwindowsid — Перетворити часовий пояс на часовий пояс для Windows

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public static IntlTimeZone::getWindowsID(string $timezoneId): string|false
```

Процедурний стиль:

```methodsynopsis
intltz_get_windows_id(string $timezoneId): string|false
```

Перекладає системний часовий пояс (наприклад, «America/LosAngeles») у часовий пояс для Windows (наприклад, «Pacific Standard Time»).

> **Зауваження**: Ця функція потребує ICU версії ≥ 52.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`timezoneId`

### Значення, що повертаються

Повертає часовий пояс для Windows або **`false`** у разі виникнення помилки.

### Дивіться також

-   [IntlTimeZone::getIDForWindowsID()](intltimezone.getidforwindowsid.html) - Перетворити часовий пояс для Windows на системний часовий пояс
