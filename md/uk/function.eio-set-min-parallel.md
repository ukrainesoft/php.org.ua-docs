---
navigation:
  - function.eio-set-max-poll-time.md: « eiosetmaxpolltime
  - function.eio-stat.md: eiostat »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiosetminparallel
---
# eiosetminparallel

(PECL eio >= 0.0.1dev)

eiosetminparallel - Встановлює мінімальну кількість паралельних потоків

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

-   [eionthreads()](function.eio-nthreads.md) - Повертає кількість потоків, що використовуються в даний момент
-   [eiosetmaxidle()](function.eio-set-max-idle.md) - Встановлює максимальну кількість очікуваних потоків
-   [eiosetmaxparallel()](function.eio-set-max-parallel.md) - Встановлює максимальну кількість паралельних потоків
