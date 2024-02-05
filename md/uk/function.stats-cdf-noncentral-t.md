---
navigation:
  - function.stats-cdf-noncentral-f.md: « stats\_cdf\_noncentral\_f
  - function.stats-cdf-normal.md: stats\_cdf\_normal »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_cdf\_noncentral\_t
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_cdf\_noncentral\_t

(PECL stats >= 1.0.0)

stats\_cdf\_noncentral\_t — Обчислює один із параметрів нецентрального розподілу Стьюдента залежно від інших

### Опис

```methodsynopsis
stats_cdf_noncentral_t(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію розподілу, обернену до неї або один із параметрів нецентрального розподілу Стьюдента. Тип значення, що повертається і параметри (`par1` `par2`и`par3`) определяются параметром`which`

Наступна таблиця містить перелік того, що буде повернено функцією та значення параметрів залежно від `which`. CDF, x, nu та mu позначають функцію кумулятивного розподілу, значення випадкової змінної, ступеня свободи та параметр нецентральності відповідно.

**Значення, що повертаються, і параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
| --- | --- | --- | --- | --- |
|  | CDF | x | nu | mu |
|  | x | CDF | nu | mu |
| 3 | nu | x | CDF | mu |
| 4 | mu | x | CDF | nu |

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

Повертає CDF, x, nu чи mu, залежно від `which`
