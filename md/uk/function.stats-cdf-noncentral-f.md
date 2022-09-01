---
navigation:
  - function.stats-cdf-noncentral-chisquare.html: « statscdfnoncentralchisquare
  - function.stats-cdf-noncentral-t.html: statscdfnoncentralt »
  - index.html: PHP Manual
  - ref.stats.html: Функції статистики
title: statscdfnoncentralф
---
# statscdfnoncentralф

(PECL stats >= 1.0.0)

statscdfnoncentralf — Обчислює один із параметрів нецентрального розподілу Фішера за іншими

### Опис

```methodsynopsis
stats_cdf_noncentral_f(    float $par1,    float $par2,    float $par3,    float $par4,    int $which): float
```

Повертає кумулятивну функцію нецентрального розподілу Фішера, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` `par2` `par3`, і `par4`) визначаються параметром `which`

У наступній таблиці перераховані значення, що повертаються, і параметри в залежності від `which`. CDF, x, nu1, nu2 та lambda позначає функцію кумулятивного розподілу, значення випадкової змінної, ступеня свободи та параметр нецентральності відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` | `par4` |
| --- | --- | --- | --- | --- | --- |
|  | CDF | з | nu1 | nu2 | lambda |
|  | з | CDF | nu1 | nu2 | lambda |
|  | nu1 | з | CDF | nu2 | lambda |
|  | nu2 | з | CDF | nu1 | lambda |
|  | lambda | з | CDF | nu1 | nu2 |

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
