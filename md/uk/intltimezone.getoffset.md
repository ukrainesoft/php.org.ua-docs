Отримати необроблене значення часового поясу та усунення за Грінвічем (GMT) за заданим моментом часу

-   [« IntlTimeZone::getIDForWindowsID](intltimezone.getidforwindowsid.md)
    
-   [IntlTimeZone::getRawOffset »](intltimezone.getrawoffset.md)
    
-   [PHP Manual](index.md)
    
-   [IntlTimeZone](class.intltimezone.md)
    
-   Отримати необроблене значення часового поясу та усунення за Грінвічем (GMT) за заданим моментом часу
    

# IntlTimeZone::getOffset

# intltzgetoffset

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlTimeZone::getOffset -- intltzgetoffset — Отримати необроблене значення часового поясу та усунення за Гринвічем (GMT) за заданим моментом часу

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

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`timestamp`

`local`

`rawOffset`

`dstOffset`

### Значення, що повертаються