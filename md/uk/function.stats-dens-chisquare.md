---
navigation:
  - function.stats-dens-cauchy.md: « stats\_dens\_cauchy
  - function.stats-dens-exponential.md: stats\_dens\_exponential »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_chisquare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_chisquare

(PECL stats >= 1.0.0)

stats\_dens\_chisquare - Щільність ймовірності розподілу хі-квадрат

### Опис

```methodsynopsis
stats_dens_chisquare(float $x, float $dfr): float
```

Повертає щільність ймовірності для `x`, где`dfr` відбиває ступеня свободи.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`dfr`

Ступені свободи

### Значення, що повертаються

Щільність ймовірності для `x`или\*\*`false`\*\*в случае возникновения ошибки.
