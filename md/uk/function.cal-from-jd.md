---
navigation:
  - function.cal-days-in-month.html: « caldaysінmonth
  - function.cal-info.html: calinfo »
  - index.html: PHP Manual
  - ref.calendar.html: Календарь
title: calfromжд
---
# calfromжд

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

calfromjd — Перетворює дату, задану в юліанському календарі, на дату вказаного календаря

### Опис

```methodsynopsis
cal_from_jd(int $julian_day, int $calendar): array
```

**calfromjd()** перетворює дату юліанського календаря, задану в `julian_day`, у дату вказаного календаря `calendar`. Підтримувані значення `calendar` **`CAL_GREGORIAN`** **`CAL_JULIAN`** **`CAL_JEWISH`** і **`CAL_FRENCH`**

### Список параметрів

`julian_day`

День юліанського календаря як ціле число

`calendar`

Календар, на який потрібно перетворити дату

### Значення, що повертаються

Повертає масив, що містить інформацію про дату, таку як місяць, день, рік, день тижня (`dow`), скорочена та повна назва дня тижня, місяця та дату у формі "місяць/день/рік". День тижня варіюється від `0` (Неділя) to `6` (Субота).

### Приклади

**Приклад #1 Приклад використання **calfromjd()****

```php
<?php
$today = unixtojd(mktime(0, 0, 0, 8, 16, 2003));
print_r(cal_from_jd($today, CAL_GREGORIAN));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [date] => 8/16/2003
    [month] => 8
    [day] => 16
    [year] => 2003
    [dow] => 6
    [abbrevdayname] => Sat
    [dayname] => Saturday
    [abbrevmonth] => Aug
    [monthname] => August
)
```

### Дивіться також

-   [calтоjd()](function.cal-to-jd.html) - Перетворює задану дату на юліанську
-   [jdtofrench()](function.jdtofrench.html) - Переказує кількість днів у юліанському літочисленні в дату за французьким республіканським календарем
-   [jdtogregorian()](function.jdtogregorian.html) - Переказує кількість днів у юліанському літочисленні в дату за Григоріанським календарем
-   [jdtojewish()](function.jdtojewish.html) - Переказує кількість днів з юліанського календаря на дату за єврейським календарем
-   [jdtojulian()](function.jdtojulian.html) - Переказує кількість днів у юліанському літочисленні в дату за юліанським календарем
-   [jdtounix()](function.jdtounix.html) - Перекладає число днів у юліанському літочисленні у мітку часу Unix
