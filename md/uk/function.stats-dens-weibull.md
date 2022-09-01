---
navigation:
  - function.stats-dens-uniform.html: « statsdensuniform
  - function.stats-harmonic-mean.html: statsharmonicmean »
  - index.html: PHP Manual
  - ref.stats.html: Функції статистики
title: statsdensweibull
---
# statsdensweibull

(PECL stats >= 1.0.0)

statsdensweibull - Щільність ймовірності розподілу Вейбулла

### Опис

```methodsynopsis
stats_dens_weibull(float $x, float $a, float $b): float
```

Повертає щільність ймовірності для `x`, де `a` і `b` є параметром форми та масштабним параметром відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`a`

Параметр форми

`b`

Масштабний параметр розподілу

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.
