---
navigation:
  - function.stats-cdf-f.md: « stats\_cdf\_f
  - function.stats-cdf-laplace.md: stats\_cdf\_laplace »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_gamma
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_gamma

(PECL stats >= 1.0.0)

stats\_cdf\_gamma — Обчислює один із параметрів Гамма-розподілу за рештою

### Опис

```methodsynopsis
stats_cdf_gamma(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію Гамма-розподілу, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` `par2`и`par3`) определяются параметром`which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x, k і theta позначає функцію кумулятивного розподілу, значення випадкової змінної, коефіцієнт форми та масштабу відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
| --- | --- | --- | --- | --- |
|  | CDF | x | k | theta |
|  | x | CDF | k | theta |
| 3 | k | x | CDF | theta |
| 4 | theta | x | CDF | k |

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

Повертає CDF, x, k або theta, залежно від значення `which`
