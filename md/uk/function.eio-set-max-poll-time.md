---
navigation:
  - function.eio-set-max-poll-reqs.md: « eiosetmaxpollreqs
  - function.eio-set-min-parallel.md: eiosetminparallel »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiosetmaxpolltime
---
# eiosetmaxpolltime

(PECL eio >= 0.0.1dev)

eiosetmaxpolltime — Встановлює максимальний час виконання

### Опис

```methodsynopsis
eio_set_max_poll_time(float $nseconds): void
```

Виконання запитів зупиняється, якщо час виконання перевищує `nseconds` секунд.

### Список параметрів

`nseconds`

Кількість секунд

### Значення, що повертаються

Функція не повертає значення після виконання.
