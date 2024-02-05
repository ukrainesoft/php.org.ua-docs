---
navigation:
  - intlgregoriancalendar.construct.md: '« IntlGregorianCalendar::\_\_construct'
  - intlgregoriancalendar.createfromdatetime.md: 'IntlGregorianCalendar::createFromDateTime »'
  - index.md: PHP Manual
  - class.intlgregoriancalendar.md: IntlGregorianCalendar
title: 'IntlGregorianCalendar::createFromDate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlGregorianCalendar::createFromDate

(PHP 8 >= 8.3.0)

IntlGregorianCalendar::createFromDate — Створює новий екземпляр IntlGregorianCalendar з дати

### Опис

```methodsynopsis
public IntlGregorianCalendar::createFromDate(int $year, int $month, int $dayOfMonth): static
```

Створює новий екземпляр [IntlGregorianCalendar](class.intlgregoriancalendar.md) із дати.

### Список параметрів

`year`

Новое значение для\*\*`IntlGregorianCalendar::FIELD_YEAR`\*\*

`month`

Новое значение для\*\*`IntlGregorianCalendar::FIELD_MONTH`\*\*. Послідовність місяців починається з нуля, тобто січень позначається як 0, лютий – 1, …, грудень – 11, а грудень (якщо він є у календарі) – 12.

`dayOfMonth`

Новое значение для\*\*`IntlGregorianCalendar::FIELD_DAY_OF_MONTH`\*\*

### Значення, що повертаються

Повертає новий екземпляр [IntlGregorianCalendar](class.intlgregoriancalendar.md)

### Приклади

**Пример #1 Пример использования метода**IntlGregorianCalendar::createFromDate()\*\*\*\*

```php
<?php

$intlCalendar = IntlGregorianCalendar::createFromDate(2023, 11, 23);
var_dump($intlCalendar);
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(IntlGregorianCalendar)#1 (5) {
  ["valid"]=>
  bool(true)
  ["type"]=>
  string(9) "gregorian"
  ["timeZone"]=>
  array(4) {
    ["valid"]=>
    bool(true)
    ["id"]=>
    string(16) "Europe/Amsterdam"
    ["rawOffset"]=>
    int(3600000)
    ["currentOffset"]=>
    int(3600000)
  }
  ["locale"]=>
  string(11) "en_US_POSIX"
  ["fields"]=>
  array(23) {
    ["era"]=>
    int(1)
    ["year"]=>
    int(2023)
    ["month"]=>
    int(11)
    ["week of year"]=>
    int(51)
    ["week of month"]=>
    int(4)
    ["day of year"]=>
    int(357)
    ["day of month"]=>
    int(23)
    ["day of week"]=>
    int(7)
    ["day of week in month"]=>
    int(4)
    ["AM/PM"]=>
    int(0)
    ["hour"]=>
    int(0)
    ["hour of day"]=>
    int(0)
    ["minute"]=>
    int(0)
    ["second"]=>
    int(0)
    ["millisecond"]=>
    int(0)
    ["zone offset"]=>
    int(3600000)
    ["DST offset"]=>
    int(0)
    ["year for week of year"]=>
    int(2023)
    ["localized day of week"]=>
    int(7)
    ["extended year"]=>
    int(2023)
    ["julian day"]=>
    int(2460302)
    ["milliseconds in day"]=>
    int(0)
    ["is leap month"]=>
    int(0)
  }
}
```

### Дивіться також

-   [IntlGregorianCalendar::createFromDateTime()](intlgregoriancalendar.createfromdatetime.md) \- Створює новий екземпляр Intel GregorianCalendar з дати та часу
