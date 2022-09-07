---
navigation:
  - function.stats-cdf-normal.md: « statscdfnormal
  - function.stats-cdf-t.md: statscdft »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statscdfpoisson
---
# statscdfpoisson

(PECL stats >= 1.0.0)

statscdfpoisson — Обчислює один із параметрів розподілу Пуассона за рештою

### Опис

```methodsynopsis
stats_cdf_poisson(float $par1, float $par2, int $which): float
```

Повертає кумулятивну функцію розподілу Пуассона, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` і `par2`) визначаються параметром `which`

У наступній таблиці перераховані значення, що повертаються, і параметри в залежності від `which`. CDF, x та lambda позначає функцію кумулятивного розподілу, значення випадкової змінної та параметр розподілу Пуассона відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` |
| --- | --- | --- | --- |
|  | CDF | з | lambda |
|  | з | CDF | lambda |
|  | lambda | з | CDF |

### Список параметрів

`par1`

Перший параметр

`par2`

Другий параметр

`which`

Прапор, що визначає, що буде повернено

### Значення, що повертаються

Повертає CDF, x або lambda, залежно від значення `which`
