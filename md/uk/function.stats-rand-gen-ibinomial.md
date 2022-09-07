---
navigation:
  - function.stats-rand-gen-ibinomial-negative.md: « statsrandgenibinomialnegative
  - function.stats-rand-gen-int.md: statsrandgenint »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsrandгенibinomial
---
# statsrandгенibinomial

(PECL stats >= 1.0.0)

statsrandгенbinomial - Обчислює випадкове відхилення від біномного розподілу

### Опис

```methodsynopsis
stats_rand_gen_ibinomial(int $n, float $pp): int
```

Обчислює випадкове відхилення від біномінального розподілу із заданим числом випробувань `ndf` та ймовірністю успіху кожного випробування `pp`

### Список параметрів

`n`

Кількість випробувань

`pp`

Коефіцієнт успішності кожного випробування

### Значення, що повертаються

Випадкове відхилення
