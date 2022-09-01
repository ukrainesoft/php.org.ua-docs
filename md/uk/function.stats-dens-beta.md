---
navigation:
  - function.stats-covariance.html: « statscovariance
  - function.stats-dens-cauchy.html: statsdenscauchy »
  - index.html: PHP Manual
  - ref.stats.html: Функції статистики
title: statsdensbeta
---
# statsdensbeta

(PECL stats >= 1.0.0)

statsdensbeta - Щільність ймовірності бета-розподілу

### Опис

```methodsynopsis
stats_dens_beta(float $x, float $a, float $b): float
```

Повертає щільність ймовірності для `x`де де випадкова величина слідує за бета-розподілом, параметри форми якого є `a` і `b`

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`a`

Параметр форми

`b`

Параметр форми

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`**, у разі виникнення помилки.
