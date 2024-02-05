---
navigation:
  - function.stats-absolute-deviation.md: « stats\_absolute\_deviation
  - function.stats-cdf-binomial.md: stats\_cdf\_binomial »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_beta
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_beta

(PECL stats >= 1.0.0)

stats\_cdf\_beta — Обчислює будь-який параметр Бета-розподілу на основі інших заданих значень

### Опис

```methodsynopsis
stats_cdf_beta(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію бета-розподілу, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` `par2`и`par3`) определяются параметром`which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x, alpha та beta позначає функцію кумулятивного розподілу, значення випадкової величини та параметри форми бета-розподілу відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
| --- | --- | --- | --- | --- |
|  | CDF | x | alpha | beta |
|  | x | CDF | alpha | beta |
| 3 | alpha | x | CDF | beta |
| 4 | beta | x | CDF | alpha |

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

Повертає CDF, x, alpha чи beta, залежно від значення `which`
