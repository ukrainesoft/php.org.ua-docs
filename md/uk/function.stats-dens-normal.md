---
navigation:
  - function.stats-dens-logistic.md: « stats\_dens\_logistic
  - function.stats-dens-pmf-binomial.md: stats\_dens\_pmf\_binomial »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_normal
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_normal

(PECL stats >= 1.0.0)

stats\_dens\_normal — Повертає щільність ймовірності нормального розподілу

### Опис

```methodsynopsis
stats_dens_normal(float $x, float $ave, float $stdev): float
```

Повертає щільність ймовірності при `x`, де випадкова величина слідує за нормальним розподілом, середнє значення якого `ave`и стандартное отклонение`stdev`

### Список параметрів

`x`

Величина, для якої обчислюється щільність імовірності

`ave`

Середнє значення розподілу

`stdev`

Стандартне відхилення

### Значення, що повертаються

Щільність ймовірності для `x`или\*\*`false`\*\*в случае возникновения ошибки.
