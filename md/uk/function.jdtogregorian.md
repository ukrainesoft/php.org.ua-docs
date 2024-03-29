---
navigation:
  - function.jdtofrench.md: « jdtofrench
  - function.jdtojewish.md: jdtojewish »
  - index.md: PHP Manual
  - ref.calendar.md: Календар
title: jdtogregorian
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# jdtogregorian

(PHP 4, PHP 5, PHP 7, PHP 8)

jdtogregorian — Переказує число днів у юліанському літочисленні в дату за Григоріанським календарем

### Опис

```methodsynopsis
jdtogregorian(int $julian_day): string
```

Переказує кількість днів у юліанському літочисленні у рядок, що містить григоріанську дату у форматі "місяць/день/рік".

### Список параметрів

`julian_day`

Номер дня у юліанському літочисленні у вигляді цілого числа

### Значення, що повертаються

Дата за григоріанським календарем у вигляді рядка формату "місяць/день/рік"

### Дивіться також

-   [gregoriantojd()](function.gregoriantojd.md) \- Перетворює дату за григоріанським календарем у кількість днів у юліанському літочисленні
-   [cal\_from\_jd()](function.cal-from-jd.md) \- Перетворює дату, задану в юліанському календарі, на дату вказаного календаря
