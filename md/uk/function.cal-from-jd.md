---
navigation:
  - function.cal-days-in-month.md: « cal\_days\_in\_month
  - function.cal-info.md: cal\_info »
  - index.md: PHP Manual
  - ref.calendar.md: Календар
title: cal\_from\_jd
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cal\_from\_jd

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

cal\_from\_jd — Перетворює дату, задану в юліанському календарі, на дату вказаного календаря

### Опис

```methodsynopsis
cal_from_jd(int $julian_day, int $calendar): array
```

Функция**cal\_from\_jd()** перетворює дату юліанського календаря, задану у параметрі `julian_day`, у дату вказаного у параметрі `calendar` календаря. Підтримувані параметром `calendar`значения:**`CAL_GREGORIAN`** **`CAL_JULIAN`** **`CAL_JEWISH`** і **`CAL_FRENCH`**

### Список параметрів

`julian_day`

День юліанського календаря як ціле число.

`calendar`

Календар, який потрібно перетворити дату.

### Значення, що повертаються

Повертає масив, що містить інформацію про дату, таку як місяць, день, рік, день тижня (`dow`), скорочена та повна назва дня тижня, місяця та дату у формі "місяць/день/рік". День тижня варіюється від (воскресенье) to`6`(суббота).

### Приклади

**Приклад #1 Приклад використання** cal\_from\_jd()\*\*\*\*

```php
<?php
$today = unixtojd(mktime(0, 0, 0, 8, 16, 2003));
print_r(cal_from_jd($today, CAL_GREGORIAN));
?>
```

Результат виконання наведеного прикладу:

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

-   [cal\_to\_jd()](function.cal-to-jd.md) \- Перетворює задану дату на юліанську
-   [jdtofrench()](function.jdtofrench.md) \- Переказує кількість днів у юліанському літочисленні в дату за французьким республіканським календарем
-   [jdtogregorian()](function.jdtogregorian.md) \- Переказує кількість днів у юліанському літочисленні в дату за Григоріанським календарем
-   [jdtojewish()](function.jdtojewish.md) \- Переказує кількість днів з юліанського календаря на дату за єврейським календарем
-   [jdtojulian()](function.jdtojulian.md) \- Переказує кількість днів у юліанському літочисленні в дату за юліанським календарем
-   [jdtounix()](function.jdtounix.md) \- Переказує кількість днів у юліанському літочисленні у мітку часу Unix
