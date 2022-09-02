---
navigation:
  - function.stats-rand-gen-noncentral-chisquare.md: « statsrandgennoncentralchisquare
  - function.stats-rand-gen-noncentral-t.md: statsrandgennoncentralt »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsrandгенnoncentralф
---
# statsrandгенnoncentralф

(PECL stats >= 1.0.0)

statsrandгенnoncentralf — Обчислює випадкове відхилення від нецентрального розподілу Фішера

### Опис

```methodsynopsis
stats_rand_gen_noncentral_f(float $dfn, float $dfd, float $xnonc): float
```

Обчислює випадкове відхилення від нецентрального розподілу Фішера із заданими числами ступенів свободи чисельника `dfn` та знаменника `dfd` та параметром зсуву `xnonc`

### Список параметрів

`dfn`

Кількість ступенів свободи чисельника

`dfd`

Кількість ступенів свободи знаменника

`xnonc`

Параметр зсуву

### Значення, що повертаються

Випадкове відхилення
