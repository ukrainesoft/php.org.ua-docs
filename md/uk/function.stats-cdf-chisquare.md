---
navigation:
  - function.stats-cdf-cauchy.md: « stats\_cdf\_cauchy
  - function.stats-cdf-exponential.md: stats\_cdf\_exponential »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_chisquare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_chisquare

(PECL stats >= 1.0.0)

stats\_cdf\_chisquare - Обчислює один з параметрів розподілу хі-квадрат за іншими

### Опис

```methodsynopsis
stats_cdf_chisquare(float $par1, float $par2, int $which): float
```

Повертає кумулятивну функцію розподілу хі-квадрат, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1`и`par2`) определяются параметром`which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x і k означає функцію кумулятивного розподілу, значення випадкової змінної та ступеня свободи відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` |
| --- | --- | --- | --- |
|  | CDF | x | k |
|  | x | CDF | k |
| 3 | k | x | CDF |

### Список параметрів

`par1`

Перший параметр

`par2`

Другий параметр

`which`

Прапор, що визначає, що буде повернено

### Значення, що повертаються

Повертає CDF, x чи k, залежно від значення `which`
