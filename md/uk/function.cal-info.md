---
navigation:
  - function.cal-from-jd.md: « calfromжд
  - function.cal-to-jd.md: calтоjd »
  - index.md: PHP Manual
  - ref.calendar.md: Календарь
title: calinfo
---
# calinfo

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

calinfo — Повертає інформацію про заданий календар

### Опис

```methodsynopsis
cal_info(int $calendar = -1): array
```

**calinfo()** повертає інформацію про заданий календар `calendar`

Інформація про календар повертається у вигляді масиву з елементами `calname` `calsymbol` `month` `abbrevmonth` і `maxdaysinmonth` В якості `calendar` можуть бути використані такі назви календарів:

-   0 або **`CAL_GREGORIAN`** - Григоріанський календар
-   1 або **`CAL_JULIAN`** - Юліанський календар
-   2 or **`CAL_JEWISH`** - Єврейський календар
-   3 or **`CAL_FRENCH`** - Календар з дня Французької революції

Якщо параметр `calendar` не заданий, повертається інформація про всі підтримувані календарі у вигляді масиву.

### Список параметрів

`calendar`

Календар, про який буде повернено інформацію. Якщо параметр не встановлено, повертається інформація про всі календарі.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад **calinfo()****

```php
<?php
$info = cal_info(0);
print_r($info);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [months] => Array
        (
            [1] => January
            [2] => February
            [3] => March
            [4] => April
            [5] => May
            [6] => June
            [7] => July
            [8] => August
            [9] => September
            [10] => October
            [11] => November
            [12] => December
        )

    [abbrevmonths] => Array
        (
            [1] => Jan
            [2] => Feb
            [3] => Mar
            [4] => Apr
            [5] => May
            [6] => Jun
            [7] => Jul
            [8] => Aug
            [9] => Sep
            [10] => Oct
            [11] => Nov
            [12] => Dec
        )

    [maxdaysinmonth] => 31
    [calname] => Gregorian
    [calsymbol] => CAL_GREGORIAN
)
```
