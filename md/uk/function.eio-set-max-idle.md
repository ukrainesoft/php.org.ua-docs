---
navigation:
  - function.eio-sendfile.html: « eiosendfile
  - function.eio-set-max-parallel.html: eiosetmaxparallel »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiosetmaxidle
---
# eiosetmaxidle

(PECL eio >= 0.0.1dev)

eiosetmaxidle — Встановлює максимальну кількість потоків, що очікують.

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

-   [eionthreads()](function.eio-nthreads.md) - Повертає кількість потоків, що використовуються в даний момент
-   [eiosetminparallel()](function.eio-set-min-parallel.md) - Встановлює мінімальну кількість паралельних потоків
-   [eiosetmaxparallel()](function.eio-set-max-parallel.md) - Встановлює максимальну кількість паралельних потоків
