---
navigation:
  - function.stats-kurtosis.md: « stats\_kurtosis
  - function.stats-rand-gen-chisquare.md: stats\_rand\_gen\_chisquare »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_rand\_gen\_beta
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_rand\_gen\_beta

(PECL stats >= 1.0.0)

stats\_rand\_gen\_beta - Обчислює випадкове відхилення від бета-розподілу

### Опис

```methodsynopsis
stats_rand_gen_beta(float $a, float $b): float
```

Повертає випадкове відхилення від Бета-розподілу з параметрами A та B. Щільність розподілу дорівнює x^(a-1) \* (1-x)^(b-1) / B(a,b) для 0 < x <. Метод R. C. H. Cheng.

### Список параметрів

`a`

Параметр форми

`b`

Параметр форми

### Значення, що повертаються

Випадкове відхилення
