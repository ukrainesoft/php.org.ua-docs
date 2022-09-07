---
navigation:
  - function.stats-dens-chisquare.md: « statsdenschisquare
  - function.stats-dens-f.md: statsdensf »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsdensexponential
---
# statsdensexponential

(PECL stats >= 1.0.0)

statsdensexponential - Щільність ймовірності експоненційного розподілу

### Опис

```methodsynopsis
stats_dens_exponential(float $x, float $scale): float
```

Повертає щільність ймовірності для `x`, де `scale` є масштабним параметром.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`scale`

Масштабний параметр розподілу

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.
