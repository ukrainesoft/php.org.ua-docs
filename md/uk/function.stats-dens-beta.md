---
navigation:
  - function.stats-covariance.md: « stats\_covariance
  - function.stats-dens-cauchy.md: stats\_dens\_cauchy »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_beta
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_beta

(PECL stats >= 1.0.0)

stats\_dens\_beta - Щільність ймовірності бета-розподілу

### Опис

```methodsynopsis
stats_dens_beta(float $x, float $a, float $b): float
```

Повертає щільність ймовірності для `x`де де випадкова величина слідує за бета-розподілом, параметри форми якого є `a`и`b`

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`a`

Параметр форми

`b`

Параметр форми

### Значення, що повертаються

Щільність ймовірності для `x`или\*\*`false`\*\*, у разі виникнення помилки.
