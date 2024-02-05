---
navigation:
  - function.eio-nreqs.md: « eio\_nreqs
  - function.eio-open.md: eio\_open »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_nthreads
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_nthreads

(PECL eio >= 0.0.1dev)

eio\_nthreads — Повертає кількість потоків, що використовуються в даний момент

### Опис

```methodsynopsis
eio_nthreads(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**eio\_nthreads()** повертає кількість потоків, що використовуються в даний момент.

### Дивіться також

-   [eio\_npending()](function.eio-npending.md) \- Повертає кількість завершених, але необроблених процесів
-   [eio\_nready()](function.eio-nready.md) \- Повертає кількість ще не опрацьованих запитів
-   [eio\_nreqs()](function.eio-nreqs.md) \- Повертає кількість запитів, які потрібно виконати
-   [eio\_set\_max\_idle()](function.eio-set-max-idle.md) \- Встановлює максимальну кількість очікуваних потоків
-   [eio\_set\_max\_parallel()](function.eio-set-max-parallel.md) \- Встановлює максимальну кількість паралельних потоків
-   [eio\_set\_min\_parallel()](function.eio-set-min-parallel.md) \- Встановлює мінімальну кількість паралельних потоків
