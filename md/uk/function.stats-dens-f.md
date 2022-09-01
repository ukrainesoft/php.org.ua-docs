---
navigation:
  - function.stats-dens-exponential.html: « statsdensexponential
  - function.stats-dens-gamma.html: statsdensgamma »
  - index.html: PHP Manual
  - ref.stats.html: Функції статистики
title: statsdensф
---
# statsdensф

(PECL stats >= 1.0.0)

statsdensf - Щільність ймовірності розподілу Фішера

### Опис

```methodsynopsis
stats_dens_f(float $x, float $dfr1, float $dfr2): float
```

Повертає щільність ймовірності для `x`, де `dfr1` і `dfr2` відбивають ступеня свободи.

### Список параметрів

`x`

Значення, для якого вважається щільність ймовірності

`dfr1`

Ступені свободи

`dfr2`

Ступені свободи

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.
