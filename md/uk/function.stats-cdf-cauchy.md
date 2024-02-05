---
navigation:
  - function.stats-cdf-binomial.md: « stats\_cdf\_binomial
  - function.stats-cdf-chisquare.md: stats\_cdf\_chisquare »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_cauchy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_cauchy

(PECL stats >= 1.0.0)

stats\_cdf\_cauchy — Обчислює один із параметрів розподілу Коші за іншими

### Опис

```methodsynopsis
stats_cdf_cauchy(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію розподілу Коші, обернену їй або один із своїх параметрів. Вигляд значення і параметрів (`par1` `par2`и`par3`) определяются параметром`which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x, x0 та gamma позначає функцію кумулятивного розподілу, значення випадкової змінної, параметр зсуву та масштабу відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
| --- | --- | --- | --- | --- |
|  | CDF | x | x0 | gamma |
|  | x | CDF | x0 | gamma |
| 3 | x0 | x | CDF | gamma |
| 4 | gamma | x | CDF | x0 |

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

Повертає CDF, x, x0 або gamma залежно від значення `which`
