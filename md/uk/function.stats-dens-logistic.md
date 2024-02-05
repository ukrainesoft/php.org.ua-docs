---
navigation:
  - function.stats-dens-laplace.md: « stats\_dens\_laplace
  - function.stats-dens-normal.md: stats\_dens\_normal »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_logistic
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_logistic

(PECL stats >= 1.0.0)

stats\_dens\_logistic - Щільність ймовірності логістичного розподілу

### Опис

```methodsynopsis
stats_dens_logistic(float $x, float $ave, float $stdev): float
```

Повертає щільність ймовірності для `x`, где`ave`и`stdev` є коефіцієнтом зсуву та логістичним розподілом відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`ave`

Коефіцієнт зсуву

`stdev`

Параметр форми

### Значення, що повертаються

Щільність ймовірності для `x`или\*\*`false`\*\*в случае возникновения ошибки.
