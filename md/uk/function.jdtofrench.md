---
navigation:
  - function.jdmonthname.md: « jdmonthname
  - function.jdtogregorian.md: jdtogregorian »
  - index.md: PHP Manual
  - ref.calendar.md: Календар
title: jdtofrench
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# jdtofrench

(PHP 4, PHP 5, PHP 7, PHP 8)

jdtofrench — Переказує кількість днів у юліанському літочисленні в дату за французьким республіканським календарем.

### Опис

```methodsynopsis
jdtofrench(int $julian_day): string
```

Переказує кількість днів у юліанському літочисленні в дату за французьким республіканським календарем

### Список параметрів

`julian_day`

Номер дня в юліанському літочисленні

### Значення, що повертаються

Дата від дня французької революції у вигляді рядка формату "місяць/день/рік"

### Дивіться також

-   [frenchtojd()](function.frenchtojd.md) \- Перетворює дату Французького республіканського календаря на кількість днів у Юліанському літочисленні
-   [cal\_from\_jd()](function.cal-from-jd.md) \- Перетворює дату, задану в юліанському календарі, на дату вказаного календаря
