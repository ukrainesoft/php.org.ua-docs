---
navigation:
  - function.stats-cdf-normal.md: « stats\_cdf\_normal
  - function.stats-cdf-t.md: stats\_cdf\_t »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_poisson
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_poisson

(PECL stats >= 1.0.0)

stats\_cdf\_poisson — Обчислює один із параметрів розподілу Пуассона за рештою

### Опис

```methodsynopsis
stats_cdf_poisson(float $par1, float $par2, int $which): float
```

Повертає кумулятивну функцію розподілу Пуассона, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1`и`par2`) определяются параметром`which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x і lambda означає функцію кумулятивного розподілу, значення випадкової змінної та параметр розподілу Пуассона відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` |
| --- | --- | --- | --- |
|  | CDF | x | lambda |
|  | x | CDF | lambda |
| 3 | lambda | x | CDF |

### Список параметрів

`par1`

Перший параметр

`par2`

Другий параметр

`which`

Прапор, що визначає, що буде повернено

### Значення, що повертаються

Повертає CDF, x або lambda, залежно від значення `which`
