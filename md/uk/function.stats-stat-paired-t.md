---
navigation:
  - function.stats-stat-innerproduct.md: « statsstatinnerproduct
  - function.stats-stat-percentile.md: statsstatpercentile »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsстатиpairedт
---
# statsстатиpairedт

(PECL stats >= 1.0.0)

statsстатиpairedt — Отримати значення t для двовибіркового t-критерію Стьюдента для залежних вибірок

### Опис

```methodsynopsis
stats_stat_paired_t(array $arr1, array $arr2): float
```

Повертає значення t для двовибіркового t-критерію Стьюдента для залежних вибірок `arr1` і `arr2`

### Список параметрів

`arr1`

Перша вибірка

`arr2`

Друга вибірка

### Значення, що повертаються

Повертає значення t або **`false`** у разі виникнення помилки.
