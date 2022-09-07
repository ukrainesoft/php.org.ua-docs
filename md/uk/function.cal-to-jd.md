---
navigation:
  - function.cal-info.md: « calinfo
  - function.easter-date.md: easterdate »
  - index.md: PHP Manual
  - ref.calendar.md: Календарь
title: calтожд
---
# calтожд

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

calтоjd - Перетворює задану дату на юліанську

### Опис

```methodsynopsis
cal_to_jd(    int $calendar,    int $month,    int $day,    int $year): int
```

**calтоjd()** розраховує кількість днів у юліанському календарі для дати у зазначеному календарі `calendar`. Список календарів, що підтримуються `calendar` **`CAL_GREGORIAN`** **`CAL_JULIAN`** **`CAL_JEWISH`** і **`CAL_FRENCH`**

### Список параметрів

`calendar`

Календар, з якого буде зроблено конвертацію, одна з констант: **`CAL_GREGORIAN`** **`CAL_JULIAN`** **`CAL_JEWISH`** або **`CAL_FRENCH`**

`month`

Місяць у вигляді числа, дозволений діапазон залежить від календаря `calendar`

`day`

День у вигляді числа, дозволений діапазон залежить від календаря `calendar`

`year`

Рік у вигляді числа, дозволений діапазон залежить від календаря `calendar`

### Значення, що повертаються

Кількість днів у юліанському календарі.

### Дивіться також

-   [calfromjd()](function.cal-from-jd.md) - Перетворює дату, задану в юліанському календарі, на дату вказаного календаря
-   [frenchtojd()](function.frenchtojd.md) - Перетворює дату Французького республіканського календаря на кількість днів у Юліанському літочисленні
-   [gregoriantojd()](function.gregoriantojd.md) - Перетворює дату за григоріанським календарем на кількість днів у юліанському літочисленні
-   [jewishtojd()](function.jewishtojd.md) - Переказує дату за єврейським календарем у число днів у юліанському літочисленні
-   [juliantojd()](function.juliantojd.md) - Переказує дату за юліанським календарем у число днів у юліанському літочисленні
-   [unixtojd()](function.unixtojd.md) - Перекладає мітку часу Unix у юліанський день
