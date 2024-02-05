---
navigation:
  - function.eio-sendfile.md: « eio\_sendfile
  - function.eio-set-max-parallel.md: eio\_set\_max\_parallel »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_set\_max\_idle
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_set\_max\_idle

(PECL eio >= 0.0.1dev)

eio\_set\_max\_idle — Встановлює максимальну кількість потоків, що очікують.

### Опис

```methodsynopsis
eio_set_max_idle(int $nthreads): void
```

### Список параметрів

`nthreads`

Кількість потоків, що простоюють.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [eio\_nthreads()](function.eio-nthreads.md) \- Повертає кількість потоків, що використовуються в даний момент
-   [eio\_set\_min\_parallel()](function.eio-set-min-parallel.md) \- Встановлює мінімальну кількість паралельних потоків
-   [eio\_set\_max\_parallel()](function.eio-set-max-parallel.md) \- Встановлює максимальну кількість паралельних потоків
