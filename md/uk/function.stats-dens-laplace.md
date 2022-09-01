---
navigation:
  - function.stats-dens-gamma.html: « statsdensgamma
  - function.stats-dens-logistic.html: statsdenslogistic »
  - index.html: PHP Manual
  - ref.stats.html: Функції статистики
title: statsdenslaplace
---
# statsdenslaplace

(PECL stats >= 1.0.0)

statsdenslaplace - Щільність ймовірності розподілу Лапласа

### Опис

```methodsynopsis
stats_dens_laplace(float $x, float $ave, float $stdev): float
```

Повертає щільність ймовірності для `x`, де `ave` і `stdev` є коефіцієнтом зсуву та параметром форми відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`ave`

Коефіцієнт зсуву

`stdev`

Параметр форми

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.
