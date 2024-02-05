---
navigation:
  - function.stats-cdf-gamma.md: « stats\_cdf\_gamma
  - function.stats-cdf-logistic.md: stats\_cdf\_logistic »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_laplace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_laplace

(PECL stats >= 1.0.0)

stats\_cdf\_laplace — Обчислює один із параметрів розподілу Лапласа за іншими

### Опис

```methodsynopsis
stats_cdf_laplace(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію розподілу Лапласа, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` `par2`и`par3`) определяются параметром`which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x, mu та b позначає функцію кумулятивного розподілу, значення випадкової змінної, параметр зсуву та масштабу відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
| --- | --- | --- | --- | --- |
|  | CDF | x | mu | b |
|  | x | CDF | mu | b |
| 3 | mu | x | CDF | b |
| 4 | b | x | CDF | mu |

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

Повертає CDF, x, mu чи b, залежно від значення `which`
