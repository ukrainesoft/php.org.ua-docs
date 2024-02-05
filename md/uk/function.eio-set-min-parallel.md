---
navigation:
  - function.eio-set-max-poll-time.md: « eio\_set\_max\_poll\_time
  - function.eio-stat.md: eio\_stat »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_set\_min\_parallel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_set\_min\_parallel

(PECL eio >= 0.0.1dev)

eio\_set\_min\_parallel - Встановлює мінімальну кількість паралельних потоків

### Опис

```methodsynopsis
eio_set_min_parallel(string $nthreads): void
```

### Список параметрів

`nthreads`

Кількість паралельних потоків.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [eio\_nthreads()](function.eio-nthreads.md) \- Повертає кількість потоків, що використовуються в даний момент
-   [eio\_set\_max\_idle()](function.eio-set-max-idle.md) \- Встановлює максимальну кількість очікуваних потоків
-   [eio\_set\_max\_parallel()](function.eio-set-max-parallel.md) \- Встановлює максимальну кількість паралельних потоків
