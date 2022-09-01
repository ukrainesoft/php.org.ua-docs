---
navigation:
  - function.stats-absolute-deviation.html: « statsabsolutedeviation
  - function.stats-cdf-binomial.html: statscdfbinomial »
  - index.html: PHP Manual
  - ref.stats.html: Функції статистики
title: statscdfbeta
---
# statscdfbeta

(PECL stats >= 1.0.0)

statscdfbeta — Обчислює будь-який параметр Бета-розподілу на основі інших заданих значень

### Опис

```methodsynopsis
stats_cdf_beta(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію бета-розподілу, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` `par2` і `par3`) визначаються параметром `which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x, alpha та beta позначає функцію кумулятивного розподілу, значення випадкової величини та параметри форми бета-розподілу відповідно.

**Значення, що повертається і параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
| --- | --- | --- | --- | --- |
|  | CDF | з | alpha | beta |
|  | з | CDF | alpha | beta |
|  | alpha | з | CDF | beta |
|  | beta | з | CDF | alpha |

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
