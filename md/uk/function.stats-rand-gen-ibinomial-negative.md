---
navigation:
  - function.stats-rand-gen-gamma.md: « statsrandgengamma
  - function.stats-rand-gen-ibinomial.md: statsrandgenibinomial »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsrandгенibinomialnegative
---
# statsrandгенibinomialnegative

(PECL stats >= 1.0.0)

statsrandгенibinomialnegative - Обчислює випадкове відхилення від негативного біномінального розподілу

### Опис

```methodsynopsis
stats_rand_gen_ibinomial_negative(int $n, float $p): int
```

Обчислює випадкове відхилення від негативного біномінального розподілу із заданим числом успішних випробувань `n` та коефіцієнтом успішності `p`

### Список параметрів

`n`

Кількість успішних випробувань

`p`

Коефіцієнт успішності

### Значення, що повертаються

Випадкове відхилення, яке є кількістю невдалих випробувань
