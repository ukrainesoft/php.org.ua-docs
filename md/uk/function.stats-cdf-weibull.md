---
navigation:
  - function.stats-cdf-uniform.md: « stats\_cdf\_uniform
  - function.stats-covariance.md: stats\_covariance »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_weibull
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_weibull

(PECL stats >= 1.0.0)

stats\_cdf\_weibull — Обчислює один із параметрів розподілу Вейбулла за рештою

### Опис

```methodsynopsis
stats_cdf_weibull(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію розподілу Вейбулла, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` `par2`и`par3`) определяются параметром`which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x, k і lambda позначає функцію кумулятивного розподілу, величину випадкової змінної, коефіцієнт форми та масштабу відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
| --- | --- | --- | --- | --- |
|  | CDF | x | k | lambda |
|  | x | CDF | k | lambda |
| 3 | k | x | CDF | lambda |
| 4 | lambda | x | CDF | k |

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

Повертає CDF, x, k або lambda, залежно від значення `which`
