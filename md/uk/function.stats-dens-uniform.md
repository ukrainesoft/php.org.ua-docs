---
navigation:
  - function.stats-dens-t.md: « stats\_dens\_t
  - function.stats-dens-weibull.md: stats\_dens\_weibull »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_dens\_uniform
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_dens\_uniform

(PECL stats >= 1.0.0)

stats\_dens\_uniform - Функція щільності ймовірності рівномірного розподілу

### Опис

```methodsynopsis
stats_dens_uniform(float $x, float $a, float $b): float
```

Повертає щільність ймовірності у `x`, где нижняя граница задана в`a`, а верхня в `b`

### Список параметрів

`x`

Значення якого обчислюватиметься щільність ймовірності

`a`

Нижній кордон розподілу

`b`

Верхня межа розподілу

### Значення, що повертаються

Щільність ймовірності в `x`или\*\*`false`\*\*в случае возникновения ошибки.
