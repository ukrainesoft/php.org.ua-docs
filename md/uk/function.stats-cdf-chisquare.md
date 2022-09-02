---
navigation:
  - function.stats-cdf-cauchy.md: « statscdfcauchy
  - function.stats-cdf-exponential.md: statscdfexponential »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statscdfchisquare
---
# statscdfchisquare

(PECL stats >= 1.0.0)

statscdfchisquare - Обчислює один з параметрів розподілу хі-квадрат за іншими

### Опис

```methodsynopsis
stats_cdf_chisquare(float $par1, float $par2, int $which): float
```

Повертає кумулятивну функцію розподілу хі-квадрат, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` і `par2`) визначаються параметром `which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x і k означає функцію кумулятивного розподілу, значення випадкової змінної та ступеня свободи відповідно.

**Значення, що повертається і параметри**

| `which` | Возвращаемое значение | `par1` | `par2` |
| --- | --- | --- | --- |
|  | CDF | з | до |
|  | з | CDF | до |
|  | до | з | CDF |

### Список параметрів

`par1`

Перший параметр

`par2`

Другий параметр

`which`

Прапор, що визначає, що буде повернено

### Значення, що повертаються

Повертає CDF, x чи k, залежно від значення `which`
