---
navigation:
  - function.stats-cdf-logistic.md: « stats\_cdf\_logistic
  - function.stats-cdf-noncentral-chisquare.md: stats\_cdf\_noncentral\_chisquare »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_negative\_binomial
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_negative\_binomial

(PECL stats >= 1.0.0)

stats\_cdf\_negative\_binomial — Обчислює один із параметрів Негативного Біномінального розподілу за іншими

### Опис

```methodsynopsis
stats_cdf_negative_binomial(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію негативного біномінального розподілу, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` `par2`и`par3`) определяются параметром`which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x, r та p позначає функцію кумулятивного розподілу, кількість провалених випробувань, кількість успішних випробувань та коефіцієнт успіху для кожного випробування відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
| --- | --- | --- | --- | --- |
|  | CDF | x | r | p |
|  | x | CDF | r | p |
| 3 | r | x | CDF | p |
| 4 | p | x | CDF | r |

### Список параметрів

`par1`

Перший параметр

`par2`

Другий параметр

`par3`

Третій параметр

`which`

Прапор, що визначає, що буде повернено

### Значення, що повертаються

Повертає CDF, x, r чи p, залежно від значення `which`
