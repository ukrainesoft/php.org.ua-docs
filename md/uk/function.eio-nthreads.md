---
navigation:
  - function.eio-nreqs.md: « eionreqs
  - function.eio-open.md: eioopen »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eionthreads
---
# eionthreads

(PECL eio >= 0.0.1dev)

eionthreads — Повертає кількість потоків, що використовуються в даний момент

### Опис

```methodsynopsis
eio_nthreads(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**eionthreads()** повертає кількість потоків, що використовуються в даний момент.

### Дивіться також

-   [eionpending()](function.eio-npending.md) - Повертає кількість завершених, але необроблених процесів
-   [eionready()](function.eio-nready.md) - Повертає кількість ще не опрацьованих запитів
-   [eionreqs()](function.eio-nreqs.md) - Повертає кількість запитів, які потрібно виконати
-   [eiosetmaxidle()](function.eio-set-max-idle.md) - Встановлює максимальну кількість очікуваних потоків
-   [eiosetmaxparallel()](function.eio-set-max-parallel.md) - Встановлює максимальну кількість паралельних потоків
-   [eiosetminparallel()](function.eio-set-min-parallel.md) - Встановлює мінімальну кількість паралельних потоків
