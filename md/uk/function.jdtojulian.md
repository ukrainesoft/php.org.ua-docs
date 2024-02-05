---
navigation:
  - function.jdtojewish.md: « jdtojewish
  - function.jdtounix.md: jdtounix »
  - index.md: PHP Manual
  - ref.calendar.md: Календар
title: jdtojulian
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# jdtojulian

(PHP 4, PHP 5, PHP 7, PHP 8)

jdtojulian — Переказує кількість днів у юліанському літочисленні в дату за юліанським календарем

### Опис

```methodsynopsis
jdtojulian(int $julian_day): string
```

Переказує кількість днів у юліанському літочисленні у рядок, що містить дату за юліанським календарем у форматі "місяць/день/рік".

### Список параметрів

`julian_day`

Номер дня в юліанському літочисленні

### Значення, що повертаються

Дата за юліанським календарем у вигляді рядка формату "місяць/день/рік"

### Дивіться також

-   [juliantojd()](function.juliantojd.md) \- Переказує дату за юліанським календарем у число днів у юліанському літочисленні
-   [cal\_from\_jd()](function.cal-from-jd.md) \- Перетворює дату, задану в юліанському календарі, на дату вказаного календаря
