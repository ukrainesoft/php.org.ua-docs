---
navigation:
  - function.stats-dens-laplace.html: « statsdenslaplace
  - function.stats-dens-normal.html: statsdensnormal »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsdenslogistic
---
# statsdenslogistic

(PECL stats >= 1.0.0)

statsdenslogistic - Щільність ймовірності логістичного розподілу

### Опис

```methodsynopsis
stats_dens_logistic(float $x, float $ave, float $stdev): float
```

Повертає щільність ймовірності для `x`, де `ave` і `stdev` є коефіцієнтом зсуву та логістичним розподілом відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`ave`

Коефіцієнт зсуву

`stdev`

Параметр форми

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.
