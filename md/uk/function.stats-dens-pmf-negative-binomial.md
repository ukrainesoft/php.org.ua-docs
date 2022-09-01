---
navigation:
  - function.stats-dens-pmf-hypergeometric.html: « statsdenspmfhypergeometric
  - function.stats-dens-pmf-poisson.html: statsdenspmfpoisson »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsdenspmfnegativebinomial
---
# statsdenspmfnegativebinomial

(PECL stats >= 1.0.0)

statsdenspmfnegativebinomial - Функція щільності ймовірності негативного біномінального розподілу

### Опис

```methodsynopsis
stats_dens_pmf_negative_binomial(float $x, float $n, float $pi): float
```

Повертає щільність ймовірності у `x`де число успіхів - це `n`, а ступінь успішності - `pi`

### Список параметрів

`x`

Значення, для якого обчислюватиметься щільність імовірності

`n`

Число успіхів розподілу

`pi`

Ступінь успішності

### Значення, що повертаються

Щільність ймовірності в `x` або **`false`** у разі виникнення помилки.
