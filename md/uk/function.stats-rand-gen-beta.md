---
navigation:
  - function.stats-kurtosis.md: « statskurtosis
  - function.stats-rand-gen-chisquare.md: statsrandgenchisquare »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsrandгенbeta
---
# statsrandгенbeta

(PECL stats >= 1.0.0)

statsrandгенbeta - Обчислює випадкове відхилення від бета-розподілу

### Опис

```methodsynopsis
stats_rand_gen_beta(float $a, float $b): float
```

Повертає випадкове відхилення від Бета-розподілу з параметрами A та B. Щільність розподілу дорівнює x^(a-1) (1-x)^(b-1) / B(a,b) для 0 < x <. Метод R. C. H. Cheng.

### Список параметрів

`a`

Параметр форми

`b`

Параметр форми

### Значення, що повертаються

Випадкове відхилення
