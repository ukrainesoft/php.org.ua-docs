---
navigation:
  - function.stats-cdf-laplace.md: « stats\_cdf\_laplace
  - function.stats-cdf-negative-binomial.md: stats\_cdf\_negative\_binomial »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_logistic
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_logistic

(PECL stats >= 1.0.0)

stats\_cdf\_logistic — Обчислює один із параметрів логістичного розподілу за рештою

### Опис

```methodsynopsis
stats_cdf_logistic(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію логістичного розподілу, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` `par2`и`par3`) определяются параметром`which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x, mu та s позначає функцію кумулятивного розподілу, значення випадкової змінної, параметр зсуву та масштабу відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
| --- | --- | --- | --- | --- |
|  | CDF | x | mu | s |
|  | x | CDF | mu | s |
| 3 | mu | x | CDF | s |
| 4 | s | x | CDF | mu |

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

Повертає CDF, x, mu чи s, залежно від значення `which`
