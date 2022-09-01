---
navigation:
  - function.stats-dens-beta.html: « statsdensbeta
  - function.stats-dens-chisquare.html: statsdenschisquare »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsdenscauchy
---
# statsdenscauchy

(PECL stats >= 1.0.0)

statsdenscauchy — Щільність ймовірності розподілу Коші

### Опис

```methodsynopsis
stats_dens_cauchy(float $x, float $ave, float $stdev): float
```

Повертає щільність ймовірності для `x`, де `ave` і `stdev` є коефіцієнтом зсуву та масштабним параметром відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність ймовірності

`ave`

Коефіцієнт зсуву

`stdev`

Масштабний параметр розподілу

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.
