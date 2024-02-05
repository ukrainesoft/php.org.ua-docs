---
navigation:
  - function.stats-rand-gen-exponential.md: « stats\_rand\_gen\_exponential
  - function.stats-rand-gen-funiform.md: stats\_rand\_gen\_funiform »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_rand\_gen\_f
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_rand\_gen\_f

(PECL stats >= 1.0.0)

stats\_rand\_gen\_f - Генерує випадкове відхилення від розподілу Фішера

### Опис

```methodsynopsis
stats_rand_gen_f(float $dfn, float $dfd): float
```

Генерує випадкове відхилення від розподілу Фішера з "dfn" ступенями волі у чисельнику та "dfd" ступенями волі у знаменнику. Метод: пряма генерація відношення варіантів хі-квадрат.

### Список параметрів

`dfn`

Кількість ступенів свободи чисельника

`dfd`

Кількість ступенів свободи знаменника

### Значення, що повертаються

Випадкове відхилення
