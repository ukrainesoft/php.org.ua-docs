---
navigation:
  - function.stats-rand-gen-exponential.html: « statsrandgenexponential
  - function.stats-rand-gen-funiform.html: statsrandgenfuniform »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsrandгенф
---
# statsrandгенф

(PECL stats >= 1.0.0)

statsrandгенf - Генерує випадкове відхилення від розподілу Фішера

### Опис

```methodsynopsis
stats_rand_gen_f(float $dfn, float $dfd): float
```

Генерує випадкове відхилення від розподілу Фішера з "dfn" ступенями волі у чисельнику та "dfd" ступенями волі у знаменнику. Метод: пряма генерація відношення варіантів хі-квадрат.

### Список параметрів

`dfn`

Кількість ступенів свободи чисельника

`dfd`

Кількість ступенів свободи знаменника

### Значення, що повертаються

Випадкове відхилення
