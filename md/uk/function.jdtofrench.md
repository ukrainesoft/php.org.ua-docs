---
navigation:
  - function.jdmonthname.md: « jdmonthname
  - function.jdtogregorian.md: jdtogregorian »
  - index.md: PHP Manual
  - ref.calendar.md: Календарь
title: jdtofrench
---
# jdtofrench

(PHP 4, PHP 5, PHP 7, PHP 8)

jdtofrench — Переказує число днів у юліанському літочисленні в дату за французьким республіканським календарем

### Опис

```methodsynopsis
jdtofrench(int $julian_day): string
```

Переказує кількість днів у юліанському літочисленні в дату за французьким республіканським календарем

### Список параметрів

`julianday`

Номер дня в юліанському літочисленні

### Значення, що повертаються

Дата від дня французької революції у вигляді рядка формату "місяць/день/рік"

### Дивіться також

-   [frenchtojd()](function.frenchtojd.md) - Перетворює дату Французького республіканського календаря на кількість днів у Юліанському літочисленні
-   [calfromjd()](function.cal-from-jd.md) - Перетворює дату, задану в юліанському календарі, на дату вказаного календаря
