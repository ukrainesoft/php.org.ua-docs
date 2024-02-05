---
navigation:
  - function.stats-cdf-negative-binomial.md: « stats\_cdf\_negative\_binomial
  - function.stats-cdf-noncentral-f.md: stats\_cdf\_noncentral\_f »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_noncentral\_chisquare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_noncentral\_chisquare

(PECL stats >= 1.0.0)

stats\_cdf\_noncentral\_chisquare - Обчислює один з параметрів нецентрального розподілу хі-квадрат за іншими

### Опис

```methodsynopsis
stats_cdf_noncentral_chisquare(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію нецентрального розподілу хі-квадрат, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` `par2`и`par3`) определяются параметром`which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x, k та lambda позначає функцію кумулятивного розподілу, значення випадкової змінної, ступеня свободи та параметр нецентральності відповідно.

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
