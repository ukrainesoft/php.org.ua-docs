---
navigation:
  - function.stats-dens-normal.md: « stats\_dens\_normal
  - function.stats-dens-pmf-hypergeometric.md: stats\_dens\_pmf\_hypergeometric »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_pmf\_binomial
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_pmf\_binomial

(PECL stats >= 1.0.0)

stats\_dens\_pmf\_binomial - Імовірнісний захід біномінального розподілу

### Опис

```methodsynopsis
stats_dens_pmf_binomial(float $x, float $n, float $pi): float
```

Повертає щільність ймовірності для `x`, где`n`и`pi` є кількістю спроб та коефіцієнтом успішності відповідно.

### Список параметрів

`x`

Значення, для якого вважається імовірнісний захід

`n`

Кількість випробувань

`pi`

Коефіцієнт успішності

### Значення, що повертаються

Імовірнісний захід для `x`или\*\*`false`\*\*в случае возникновения ошибки.
