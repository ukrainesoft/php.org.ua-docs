---
navigation:
  - function.stats-cdf-noncentral-t.md: « stats\_cdf\_noncentral\_t
  - function.stats-cdf-poisson.md: stats\_cdf\_poisson »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_normal
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_normal

(PECL stats >= 1.0.0)

stats\_cdf\_normal — обчислює один із параметрів розподілу залежно від інших

### Опис

```methodsynopsis
stats_cdf_normal(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію розподілу, обернену до неї або один із параметрів нормального розподілу. Тип значення, що повертається і параметри (`par1` `par2`и`par3`) определяются параметром`which`

Наступна таблиця містить перелік того, що буде повернено функцією та значення параметрів залежно від `which`. CDF, x, mu та sigma позначають функцію розподілу, значення випадкової змінної, медіану та стандартне відхилення відповідно.

**Значення, що повертаються, і параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
| --- | --- | --- | --- | --- |
|  | CDF | x | mu | sigma |
|  | x | CDF | mu | sigma |
| 3 | mu | x | CDF | sigma |
| 4 | sigma | x | CDF | mu |

### Список параметрів

`par1`

Перший параметр

`par2`

Другий параметр

`par3`

Третій параметр

`which`

Прапор, що визначає поведінку функції

### Значення, що повертаються

Повертає CDF, x, mu чи sigma, залежно від `which`
