---
navigation:
  - function.stats-dens-pmf-negative-binomial.md: « stats\_dens\_pmf\_negative\_binomial
  - function.stats-dens-t.md: stats\_dens\_t »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_pmf\_poisson
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_pmf\_poisson

(PECL stats >= 1.0.0)

stats\_dens\_pmf\_poisson - Імовірнісний захід розподілу Пуассона

### Опис

```methodsynopsis
stats_dens_pmf_poisson(float $x, float $lb): float
```

Повертає імовірнісний захід для `x`, где`lb`является параметром распределения Пуассона.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`lb`

Параметр розподілу Пуассона

### Значення, що повертаються

Щільність ймовірності для `x`или\*\*`false`\*\*в случае возникновения ошибки.
