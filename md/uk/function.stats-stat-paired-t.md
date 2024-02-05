---
navigation:
  - function.stats-stat-innerproduct.md: « stats\_stat\_innerproduct
  - function.stats-stat-percentile.md: stats\_stat\_percentile »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_stat\_paired\_t
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_stat\_paired\_t

(PECL stats >= 1.0.0)

stats\_stat\_paired\_t — Отримати значення t для двовибіркового t-критерію Стьюдента для залежних вибірок

### Опис

```methodsynopsis
stats_stat_paired_t(array $arr1, array $arr2): float
```

Повертає значення t для двовибіркового t-критерію Стьюдента для залежних вибірок `arr1`и`arr2`

### Список параметрів

`arr1`

Перша вибірка

`arr2`

Друга вибірка

### Значення, що повертаються

Повертає значення t або \*\*`false`\*\*в случае возникновения ошибки.
