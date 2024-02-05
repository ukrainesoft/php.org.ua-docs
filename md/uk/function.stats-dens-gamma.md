---
navigation:
  - function.stats-dens-f.md: « stats\_dens\_f
  - function.stats-dens-laplace.md: stats\_dens\_laplace »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_gamma
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_gamma

(PECL stats >= 1.0.0)

stats\_dens\_gamma - Щільність ймовірності гамма-розподілу

### Опис

```methodsynopsis
stats_dens_gamma(float $x, float $shape, float $scale): float
```

Повертає щільність ймовірності для `x`, где`shape`и`scale` є коефіцієнтом форми та масштабним параметром відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`shape`

Параметр форми

`scale`

Масштабний параметр розподілу

### Значення, що повертаються

Щільність ймовірності для `x`или\*\*`false`\*\*в случае возникновения ошибки.
