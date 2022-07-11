- [«cal_from_jd](function.cal-from-jd.md)
- [cal_to_jd »](function.cal-to-jd.md)

- [PHP Manual](index.md)
- [Календарь](ref.calendar.md)
- Повертає інформацію про заданий календар

#cal_info

(PHP 4 \>= 4.1.0, PHP 5, PHP 7, PHP 8)

cal_info — Повертає інформацію про заданий календар

### Опис

**cal_info**(int `$calendar` = -1): array

**cal_info()** повертає інформацію про заданий календар `calendar`.

Інформація про календар повертається у вигляді масиву з елементами
`calname`, `calsymbol`, `month`, `abbrevmonth` та `maxdaysinmonth`
як `calendar` можуть бути використані наступні назви
календарів:

- 0 or **`CAL_GREGORIAN`** - Григоріанський календар
- 1 or **`CAL_JULIAN`** - Юліанський календар
- 2 or **`CAL_JEWISH`** - Єврейський календар
- 3 or **`CAL_FRENCH`** - Календар з дня Французької революції

Якщо параметр calendar не заданий, повертається інформація про всіх
підтримуваних календарів як масиву.

### Список параметрів

`calendar`
Календар, про який буде повернено інформацію. Якщо параметр не
заданий, повертається інформація про всі календарі.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад **cal_info()****

` <?php$info = cal_info(0);print_r($info);?> `

Результат виконання цього прикладу:

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
[10] => жовтень
[11] => Листопад
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
