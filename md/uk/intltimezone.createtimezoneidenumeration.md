Отримати перерахування з ідентифікаторів системних часових поясів за умовами фільтрації

-   [« IntlTimeZone::createTimeZone](intltimezone.createtimezone.html)
    
-   [IntlTimeZone::fromDateTimeZone »](intltimezone.fromdatetimezone.html)
    
-   [PHP Manual](index.html)
    
-   [IntlTimeZone](class.intltimezone.html)
    
-   Отримати перерахування з ідентифікаторів системних часових поясів за умовами фільтрації
    

# IntlTimeZone::createTimeZoneIDEnumeration

# intltzcreatetimezoneідenumeration

(PHP 5> = 5.5.0, PHP 7, PHP 8)

IntlTimeZone::createTimeZoneIDEnumeration -- intltzcreatetimezoneідenumeration — Отримати перерахування з ідентифікаторів системних часових поясів за умовами фільтрації

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

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`type`

`region`

`rawOffset`

### Значення, що повертаються

Повертає [IntlIterator](class.intliterator.html) або **`false`** у разі виникнення помилки.