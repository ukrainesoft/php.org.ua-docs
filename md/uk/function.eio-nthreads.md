---
navigation:
  - function.eio-nreqs.html: « eionreqs
  - function.eio-open.html: eioopen »
  - index.html: PHP Manual
  - ref.eio.html: Eio Функции
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

-   [eionpending()](function.eio-npending.html) - Повертає кількість завершених, але необроблених процесів
-   [eionready()](function.eio-nready.html) - Повертає кількість ще не опрацьованих запитів
-   [eionreqs()](function.eio-nreqs.html) - Повертає кількість запитів, які потрібно виконати
-   [eiosetmaxidle()](function.eio-set-max-idle.html) - Встановлює максимальну кількість очікуваних потоків
-   [eiosetmaxparallel()](function.eio-set-max-parallel.html) - Встановлює максимальну кількість паралельних потоків
-   [eiosetminparallel()](function.eio-set-min-parallel.html) - Встановлює мінімальну кількість паралельних потоків
