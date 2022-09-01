---
navigation:
  - function.stats-cdf-negative-binomial.html: « statscdfnegativebinomial
  - function.stats-cdf-noncentral-f.html: statscdfnoncentralf »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statscdfnoncentralchisquare
---
# statscdfnoncentralchisquare

(PECL stats >= 1.0.0)

statscdfnoncentralchisquare - Обчислює один з параметрів нецентрального розподілу хі-квадрат за іншими

### Опис

```methodsynopsis
stats_cdf_noncentral_chisquare(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію нецентрального розподілу хі-квадрат, обернену до неї або один із своїх параметрів. Вигляд значення і параметрів (`par1` `par2` і `par3`) визначаються параметром `which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x, k та lambda позначає функцію кумулятивного розподілу, значення випадкової змінної, ступеня свободи та параметр нецентральності відповідно.

**Значення, що повертається і параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
| --- | --- | --- | --- | --- |
|  | CDF | з | до | lambda |
|  | з | CDF | до | lambda |
|  | до | з | CDF | lambda |
|  | lambda | з | CDF | до |

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
