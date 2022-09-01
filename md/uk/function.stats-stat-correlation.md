---
navigation:
  - function.stats-stat-binomial-coef.html: « statsstatbinomialcoef
  - function.stats-stat-factorial.html: statsstatfactorial »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsстатиcorrelation
---
# statsстатиcorrelation

(PECL stats >= 1.0.0)

statsстатиcorrelation - Повертає коефіцієнт кореляції Пірсона двох наборів даних

### Опис

```methodsynopsis
stats_stat_correlation(array $arr1, array $arr2): float
```

Повертає коефіцієнт кореляції Пірсона для `arr1` і `arr2`

### Список параметрів

`arr1`

Перший масив

`arr2`

Другий масив

### Значення, що повертаються

Повертає коефіцієнт кореляції Пірсона для `arr1` і `arr2`, або **`false`** у разі виникнення помилки.
