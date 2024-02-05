---
navigation:
  - function.stats-cdf-noncentral-chisquare.md: « stats\_cdf\_noncentral\_chisquare
  - function.stats-cdf-noncentral-t.md: stats\_cdf\_noncentral\_t »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_noncentral\_f
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_noncentral\_f

(PECL stats >= 1.0.0)

stats\_cdf\_noncentral\_f — Обчислює один із параметрів нецентрального розподілу Фішера за іншими

### Опис

```methodsynopsis
stats_cdf_noncentral_f(    float $par1,    float $par2,    float $par3,    float $par4,    int $which): float
```

Повертає кумулятивну функцію нецентрального розподілу Фішера, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` `par2` `par3`, и`par4`) определяются параметром`which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x, nu1, nu2 та lambda позначає функцію кумулятивного розподілу, значення випадкової змінної, ступеня свободи та параметр нецентральності відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` | `par4` |
| --- | --- | --- | --- | --- | --- |
|  | CDF | x | nu1 | nu2 | lambda |
|  | x | CDF | nu1 | nu2 | lambda |
| 3 | nu1 | x | CDF | nu2 | lambda |
| 4 | nu2 | x | CDF | nu1 | lambda |
| 5 | lambda | x | CDF | nu1 | nu2 |

### Список параметрів

`par1`

Перший параметр

`par2`

Другий параметр

`par3`

Третій параметр

`par4`

Четвертий параметр

`which`

Прапор, що визначає, що буде повернено

### Значення, що повертаються

Повертає CDF, x, nu1, nu2 або lambda, залежно від значення `which`
