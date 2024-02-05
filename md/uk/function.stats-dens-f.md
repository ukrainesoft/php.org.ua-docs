---
navigation:
  - function.stats-dens-exponential.md: « stats\_dens\_exponential
  - function.stats-dens-gamma.md: stats\_dens\_gamma »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_f
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_f

(PECL stats >= 1.0.0)

stats\_dens\_f - Щільність ймовірності розподілу Фішера

### Опис

```methodsynopsis
stats_dens_f(float $x, float $dfr1, float $dfr2): float
```

Повертає щільність ймовірності для `x`, где`dfr1`и`dfr2` відбивають ступеня свободи.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`dfr1`

Ступені свободи

`dfr2`

Ступені свободи

### Значення, що повертаються

Щільність ймовірності для `x`или\*\*`false`\*\*в случае возникновения ошибки.
