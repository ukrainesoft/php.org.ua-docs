---
navigation:
  - function.stats-dens-beta.md: « stats\_dens\_beta
  - function.stats-dens-chisquare.md: stats\_dens\_chisquare »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_cauchy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_cauchy

(PECL stats >= 1.0.0)

stats\_dens\_cauchy — Щільність ймовірності розподілу Коші

### Опис

```methodsynopsis
stats_dens_cauchy(float $x, float $ave, float $stdev): float
```

Повертає щільність ймовірності для `x`, где`ave`и`stdev` є коефіцієнтом зсуву та масштабним параметром відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`ave`

Коефіцієнт зсуву

`stdev`

Масштабний параметр розподілу

### Значення, що повертаються

Щільність ймовірності для `x`или\*\*`false`\*\*в случае возникновения ошибки.
