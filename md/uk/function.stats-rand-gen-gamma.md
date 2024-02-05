---
navigation:
  - function.stats-rand-gen-funiform.md: « stats\_rand\_gen\_funiform
  - function.stats-rand-gen-ibinomial-negative.md: stats\_rand\_gen\_ibinomial\_negative »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_rand\_gen\_gamma
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_rand\_gen\_gamma

(PECL stats >= 1.0.0)

stats\_rand\_gen\_gamma - Обчислює випадкове відхилення від гамма-розподілу

### Опис

```methodsynopsis
stats_rand_gen_gamma(float $a, float $r): float
```

Згенерувати випадкове відхилення від Гамма-розподілу. Щільність розраховується за формулою (A\*\*R)/Gamma(R)\*X\*\*(R-1)\*Exp(-A\*X).

### Список параметрів

`a`

Коефіцієнт зсуву Гамма-розподілу (`a` > 0).

`r`

Коефіцієнт форми Гамма-розподілу (`r` > 0).

### Значення, що повертаються

Випадкове відхилення
