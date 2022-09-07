---
navigation:
  - function.stats-cdf-noncentral-t.md: « statscdfnoncentralт
  - function.stats-cdf-poisson.md: statscdfpoisson »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statscdfnormal
---
# statscdfnormal

(PECL stats >= 1.0.0)

statscdfnormal — обчислює один із параметрів розподілу залежно від інших

### Опис

```methodsynopsis
stats_cdf_normal(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію розподілу, обернену до неї або один із параметрів нормального розподілу. Тип значення, що повертається і параметри (`par1` `par2` і `par3`) визначаються параметром `which`

Наступна таблиця містить перелік того, що буде повернено функцією та значення параметрів залежно від `which`. CDF, x, mu та sigma позначають функцію розподілу, значення випадкової змінної, медіану та стандартне відхилення відповідно.

**Значення, що повертаються, і параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
| --- | --- | --- | --- | --- |
|  | CDF | з | му | sigma |
|  | з | CDF | му | sigma |
|  | му | з | CDF | sigma |
|  | sigma | з | CDF | му |

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
