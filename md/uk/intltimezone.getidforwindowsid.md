Перетворити часовий пояс для Windows на системний часовий пояс

-   [« IntlTimeZone::getID](intltimezone.getid.html)
    
-   [IntlTimeZone::getOffset »](intltimezone.getoffset.html)
    
-   [PHP Manual](index.html)
    
-   [IntlTimeZone](class.intltimezone.html)
    
-   Перетворити часовий пояс для Windows на системний часовий пояс
    

# IntlTimeZone::getIDForWindowsID

# intltzgetідforwindowsід

(PHP 7> = 7.1.0, PHP 8)

IntlTimeZone::getIDForWindowsID -- intltzgetідforwindowsid — Перетворити часовий пояс для Windows на системний часовий пояс

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public static IntlTimeZone::getIDForWindowsID(string $timezoneId, ?string $region = null): string|false
```

Процедурний стиль:

```methodsynopsis
intltz_get_id_for_windows_id(string $timezoneId, ?string $region = null): string|false
```

Переводить часовий пояс для Windows (наприклад, "Pacific Standard Time") у системний часовий пояс (наприклад, "America/Los"Angeles»).

> **Зауваження**: Ця функція потребує ICU версії ≥ 52.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`timezoneId`

`region`

### Значення, що повертаються

Повертає системний часовий пояс або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `region` тепер припускає значення **`null`** |

### Дивіться також

-   [IntlTimeZone::getWindowsID()](intltimezone.getwindowsid.html) - Перетворити системний часовий пояс на часовий пояс для Windows