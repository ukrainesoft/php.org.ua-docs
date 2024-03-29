---
navigation:
  - intlcalendar.getavailablelocales.md: '« IntlCalendar::getAvailableLocales'
  - intlcalendar.geterrorcode.md: 'IntlCalendar::getErrorCode »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getDayOfWeekType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::getDayOfWeekType

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getDayOfWeekType — Повідомляє, чи день буде буднім, вихідним або днем ​​з переходом між ними

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getDayOfWeekType(int $dayOfWeek): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_day_of_week_type(IntlCalendar $calendar, int $dayOfWeek): int|false
```

Повертає, чи вказаний день є робочим днем ​​(**`IntlCalendar::DOW_TYPE_WEEKDAY`**), вихідним днем ​​(**`IntlCalendar::DOW_TYPE_WEEKEND`**), днем, протягом якого відбувається перехід у вихідні (**`IntlCalendar::DOW_TYPE_WEEKEND_OFFSET`**) або день, протягом якого припиняються вихідні (**`IntlCalendar::DOW_TYPE_WEEKEND_CEASE`**

Якщо повернення або **`IntlCalendar::DOW_TYPE_WEEKEND_OFFSET`**, либо\*\*`IntlCalendar::DOW_TYPE_WEEKEND_CEASE`\*\*потім можна викликати [IntlCalendar::getWeekendTransition()](intlcalendar.getweekendtransition.md)для получения времени перехода.

Для цієї функції потрібний ICU 4.4 або новіший.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`dayOfWeek`

Одна из констант:**`IntlCalendar::DOW_SUNDAY`** **`IntlCalendar::DOW_MONDAY`** **`IntlCalendar::DOW_SATURDAY`**

### Значення, що повертаються

Повертає одну з констант: **`IntlCalendar::DOW_TYPE_WEEKDAY`** **`IntlCalendar::DOW_TYPE_WEEKEND`** \*\*`IntlCalendar::DOW_TYPE_WEEKEND_OFFSET`** або **`IntlCalendar::DOW_TYPE_WEEKEND_CEASE`** або **`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** IntlCalendar::getDayOfWeekType()\*\*\*\*

```php
<?php
foreach (array('en_US', 'ar_SA') as $locale) {
    echo "Языковой стандарт: ", Locale::getDisplayName($locale, "en_US"), "\n";

    $cal = IntlCalendar::createInstance('UTC', $locale);

    for ($i = IntlCalendar::DOW_SUNDAY; $i <= IntlCalendar::DOW_SATURDAY; $i++) {
        $type = $cal->getDayOfWeekType($i);
        $transition = ($type !== IntlCalendar::DOW_TYPE_WEEKDAY)
            ? $cal->getWeekendTransition($i)
            : '';
        echo $i, " ", $type, " ", $transition, "\n";
    }
    echo "\n";
}
?>
```

Результат виконання наведеного прикладу:

```
Языковой стандарт: English (United States)
1 1 86400000
2 0
3 0
4 0
5 0
6 0
7 1 0

Языковой стандарт: Arabic (Saudi Arabia)
1 0
2 0
3 0
4 0
5 0
6 1 0
7 1 86400000
```
