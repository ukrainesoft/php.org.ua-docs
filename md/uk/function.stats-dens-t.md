---
navigation:
  - function.stats-dens-pmf-poisson.md: « stats\_dens\_pmf\_poisson
  - function.stats-dens-uniform.md: stats\_dens\_uniform »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_t
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_t

(PECL stats >= 1.0.0)

stats\_dens\_t - Щільність ймовірності розподілу Стьюдента

### Опис

```methodsynopsis
stats_dens_t(float $x, float $dfr): float
```

Повертає щільність ймовірності для `x`, где`scale` відображає кількість ступенів свободи.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`dfr`

Ступені свободи

### Значення, що повертаються

Щільність ймовірності для `x`или\*\*`false`\*\*в случае возникновения ошибки.
