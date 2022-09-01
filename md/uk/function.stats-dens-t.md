---
navigation:
  - function.stats-dens-pmf-poisson.html: « statsdenspmfpoisson
  - function.stats-dens-uniform.html: statsdensuniform »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsdensт
---
# statsdensт

(PECL stats >= 1.0.0)

statsdenst - Щільність ймовірності розподілу Стьюдента

### Опис

```methodsynopsis
stats_dens_t(float $x, float $dfr): float
```

Повертає щільність ймовірності для `x`, де `scale` відображає кількість ступенів свободи.

### Список параметрів

`x`

Значення, для якого вважається щільність ймовірності

`dfr`

Ступені свободи

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.
