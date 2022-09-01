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

-   [eionthreads()](function.eio-nthreads.html) - Повертає кількість потоків, що використовуються в даний момент
-   [eiosetmaxidle()](function.eio-set-max-idle.html) - Встановлює максимальну кількість очікуваних потоків
-   [eiosetminparallel()](function.eio-set-min-parallel.html) - Встановлює мінімальну кількість паралельних потоків
