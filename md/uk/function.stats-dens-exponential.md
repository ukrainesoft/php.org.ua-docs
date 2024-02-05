---
navigation:
  - function.stats-dens-chisquare.md: « stats\_dens\_chisquare
  - function.stats-dens-f.md: stats\_dens\_f »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_exponential
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_exponential

(PECL stats >= 1.0.0)

stats\_dens\_exponential - Щільність ймовірності експоненційного розподілу

### Опис

```methodsynopsis
stats_dens_exponential(float $x, float $scale): float
```

Повертає щільність ймовірності для `x`, где`scale` є масштабним параметром.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`scale`

Масштабний параметр розподілу

### Значення, що повертаються

Щільність ймовірності для `x`или\*\*`false`\*\*в случае возникновения ошибки.
