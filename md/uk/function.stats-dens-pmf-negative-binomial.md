---
navigation:
  - function.stats-dens-pmf-hypergeometric.md: « stats\_dens\_pmf\_hypergeometric
  - function.stats-dens-pmf-poisson.md: stats\_dens\_pmf\_poisson »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_pmf\_negative\_binomial
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_pmf\_negative\_binomial

(PECL stats >= 1.0.0)

stats\_dens\_pmf\_negative\_binomial - Функція щільності ймовірності негативного біномінального розподілу

### Опис

```methodsynopsis
stats_dens_pmf_negative_binomial(float $x, float $n, float $pi): float
```

Повертає щільність ймовірності у `x`де число успіхів - це `n`, а степень успешности -`pi`

### Список параметрів

`x`

Значення, для якого обчислюватиметься щільність імовірності

`n`

Число успіхів розподілу

`pi`

Ступінь успішності

### Значення, що повертаються

Щільність ймовірності в `x`или\*\*`false`\*\*в случае возникновения ошибки.
