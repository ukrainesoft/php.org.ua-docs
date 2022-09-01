---
navigation:
  - function.eio-set-max-idle.html: « eiosetmaxidle
  - function.eio-set-max-poll-reqs.html: eiosetmaxpollreqs »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiosetmaxparallel
---
# eiosetmaxparallel

(PECL eio >= 0.0.1dev)

eiosetmaxparallel — Встановлює максимальну кількість паралельних потоків

### Опис

```methodsynopsis
eio_set_max_parallel(int $nthreads): void
```

### Список параметрів

`nthreads`

Кількість паралельних потоків

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [eionthreads()](function.eio-nthreads.md) - Повертає кількість потоків, що використовуються в даний момент
-   [eiosetmaxidle()](function.eio-set-max-idle.md) - Встановлює максимальну кількість очікуваних потоків
-   [eiosetminparallel()](function.eio-set-min-parallel.md) - Встановлює мінімальну кількість паралельних потоків
