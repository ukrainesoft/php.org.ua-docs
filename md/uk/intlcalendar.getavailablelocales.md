---
navigation:
  - intlcalendar.getactualminimum.md: '« IntlCalendar::getActualMinimum'
  - intlcalendar.getdayofweektype.md: 'IntlCalendar::getDayOfWeekType »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getAvailableLocales'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::getAvailableLocales

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getAvailableLocales — Отримує масив мовних стандартів, для яких є дані

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static IntlCalendar::getAvailableLocales(): array
```

Процедурний стиль

```methodsynopsis
intlcal_get_available_locales(): array
```

Надає список мовних стандартів, для яких встановлені календарі. Починаючи з ICU 51, це список усіх встановлених мовних стандартів ICU.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) рядків (string), кожен із яких відповідає мовному стандарту.

### Приклади

**Приклад #1 Приклад використання** IntlCalendar::getAvailableLocales()\*\*\*\*

```php
<?php
print_r(IntlCalendar::getAvailableLocales());
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => af
    [1] => af_NA
    [2] => af_ZA
    [3] => agq
    [4] => agq_CM
    [5] => ak
    [6] => ak_GH
    [7] => am
    [8] => am_ET
    [9] => ar
    [10] => ar_001
    [11] => ar_AE
    [12] => ar_BH
    [13] => ar_DJ
    … output abbreviated …
    [595] => zh_Hant_HK
    [596] => zh_Hant_MO
    [597] => zh_Hant_TW
    [598] => zu
    [599] => zu_ZA
)
```
