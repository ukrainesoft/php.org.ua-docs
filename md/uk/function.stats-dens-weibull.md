---
navigation:
  - function.stats-dens-uniform.md: « stats\_dens\_uniform
  - function.stats-harmonic-mean.md: stats\_harmonic\_mean »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_weibull
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_weibull

(PECL stats >= 1.0.0)

stats\_dens\_weibull - Щільність ймовірності розподілу Вейбулла

### Опис

```methodsynopsis
stats_dens_weibull(float $x, float $a, float $b): float
```

Повертає щільність ймовірності для `x`, где`a`и`b` є параметром форми та масштабним параметром відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`a`

Параметр форми

`b`

Масштабний параметр розподілу

### Значення, що повертаються

Щільність ймовірності для `x`или\*\*`false`\*\*в случае возникновения ошибки.
