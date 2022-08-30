Отримує найбільше локальне мінімальне значення поля

-   [« IntlCalendar::getFirstDayOfWeek](intlcalendar.getfirstdayofweek.md)
    
-   [IntlCalendar::getKeywordValuesForLocale »](intlcalendar.getkeywordvaluesforlocale.md)
    
-   [PHP Manual](index.md)
    
-   [IntlCalendar](class.intlcalendar.md)
    
-   Отримує найбільше локальне мінімальне значення поля
    

# IntlCalendar::getGreatestMinimum

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getGreatestMinimum — Отримує найбільше локальне мінімальне значення поля

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getGreatestMinimum(int $field): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_greatest_minimum(IntlCalendar $calendar, int $field): int|false
```

Повертає найбільше локальне мінімальне значення поля. Це має бути значення, більше або рівне значенню, що повертається [IntlCalendar::getActualMinimum()](intlcalendar.getactualminimum.md), яке, у свою чергу, більше або дорівнює значенню, що повертається [IntlCalendar::getMinimum()](intlcalendar.getminimum.md). Всі ці три функції повертають те саме значення для григоріанського календаря.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.md) [констант](class.intlcalendar.html#intlcalendar.constants) полів типу дата/час. Ціла кількість від `0` до **`IntlCalendar::FIELD_COUNT`**

### Значення, що повертаються

Ціле число (int), що представляє значення поля або **`false`** у разі виникнення помилки.