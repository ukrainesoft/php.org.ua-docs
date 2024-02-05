---
navigation:
  - function.stats-dens-pmf-binomial.md: « stats\_dens\_pmf\_binomial
  - function.stats-dens-pmf-negative-binomial.md: stats\_dens\_pmf\_negative\_binomial »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_pmf\_hypergeometric
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_pmf\_hypergeometric

(PECL stats >= 1.0.0)

stats\_dens\_pmf\_hypergeometric - Імовірнісний захід гіпергеометричного розподілу

### Опис

```methodsynopsis
stats_dens_pmf_hypergeometric(    float $n1,    float $n2,    float $N1,    float $N2): float
```

Повертає імовірнісний захід для `n1`, где`n2` `N1`и`N2` є кількістю невдалих спроб, числом успішних вибірок та числом невдалих вибірок відповідно.

### Список параметрів

`n1`

Число успішних спроб, при яких обчислюється імовірнісний захід

`n2`

Кількість невдалих спроб

`N1`

Число успішних вибірок

`N2`

Число невдалих вибірок

### Значення, що повертаються

Імовірнісний захід для `n1`или\*\*`false`\*\*в случае возникновения ошибки.
