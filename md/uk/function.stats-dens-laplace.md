---
navigation:
  - function.stats-dens-gamma.md: « stats\_dens\_gamma
  - function.stats-dens-logistic.md: stats\_dens\_logistic »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_laplace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_laplace

(PECL stats >= 1.0.0)

stats\_dens\_laplace - Щільність ймовірності розподілу Лапласа

### Опис

```methodsynopsis
stats_dens_laplace(float $x, float $ave, float $stdev): float
```

Повертає щільність ймовірності для `x`, где`ave`и`stdev` є коефіцієнтом зсуву та параметром форми відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`ave`

Коефіцієнт зсуву

`stdev`

Параметр форми

### Значення, що повертаються

Щільність ймовірності для `x`или\*\*`false`\*\*в случае возникновения ошибки.
