---
navigation:
  - intltimezone.getid.md: '« IntlTimeZone::getID'
  - intltimezone.getoffset.md: 'IntlTimeZone::getOffset »'
  - index.md: PHP Manual
  - class.intltimezone.md: IntlTimeZone
title: 'IntlTimeZone::getIDForWindowsID'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlTimeZone::getIDForWindowsID

# intltz\_get\_id\_for\_windows\_id

(PHP 7 >= 7.1.0, PHP 8)

IntlTimeZone::getIDForWindowsID -- intltz\_get\_id\_for\_windows\_id — Перетворити часовий пояс для Windows на системний часовий пояс

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public static IntlTimeZone::getIDForWindowsID(string $timezoneId, ?string $region = null): string|false
```

Процедурний стиль:

```methodsynopsis
intltz_get_id_for_windows_id(string $timezoneId, ?string $region = null): string|false
```

Переводить часовий пояс для Windows (наприклад, "Pacific Standard Time") у системний часовий пояс (наприклад, "America/Los"\_Angeles»).

> **Зауваження**: Ця функція потребує ICU версії ≥ 52.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`timezoneId`

`region`

### Значення, що повертаються

Повертає системний часовий пояс або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`region` тепер припускає значення **`null`** |

### Дивіться також

-   [IntlTimeZone::getWindowsID()](intltimezone.getwindowsid.md) \- Перетворити системний часовий пояс на часовий пояс для Windows
