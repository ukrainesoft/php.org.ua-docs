---
navigation:
  - function.stats-rand-gen-funiform.md: « statsrandgenfuniform
  - function.stats-rand-gen-ibinomial-negative.md: statsrandgenibinomialnegative »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsrandгенgamma
---
# statsrandгенgamma

(PECL stats >= 1.0.0)

statsrandгенgamma - Обчислює випадкове відхилення від гамма-розподілу

### Опис

```methodsynopsis
stats_rand_gen_gamma(float $a, float $r): float
```

Згенерувати випадкове відхилення від Гамма-розподілу. Щільність розраховується за формулою (AR)/Gamma(R) З(R-1) Exp(-AX).

### Список параметрів

`a`

Коефіцієнт зсуву Гамма-розподілу (`a` > 0).

`r`

Коефіцієнт форми Гамма-розподілу (`r` > 0).

### Значення, що повертаються

Випадкове відхилення
