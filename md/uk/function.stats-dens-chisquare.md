---
navigation:
  - function.stats-dens-cauchy.html: « statsdenscauchy
  - function.stats-dens-exponential.html: statsdensexponential »
  - index.html: PHP Manual
  - ref.stats.html: Функції статистики
title: statsdenschisquare
---
# statsdenschisquare

(PECL stats >= 1.0.0)

statsdenschisquare - Щільність ймовірності розподілу хі-квадрат

### Опис

```methodsynopsis
stats_dens_chisquare(float $x, float $dfr): float
```

Повертає щільність ймовірності для `x`, де `dfr` відбиває ступеня свободи.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`dfr`

Ступені свободи

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.
