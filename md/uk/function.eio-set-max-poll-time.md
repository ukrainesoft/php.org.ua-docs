---
navigation:
  - function.eio-set-max-poll-reqs.md: « eio\_set\_max\_poll\_reqs
  - function.eio-set-min-parallel.md: eio\_set\_min\_parallel »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_set\_max\_poll\_time
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_set\_max\_poll\_time

(PECL eio >= 0.0.1dev)

eio\_set\_max\_poll\_time — Встановлює максимальний час виконання

### Опис

```methodsynopsis
eio_set_max_poll_time(float $nseconds): void
```

Виконання запитів зупиняється, якщо час виконання перевищує `nseconds`секунд.

### Список параметрів

`nseconds`

Кількість секунд

### Значення, що повертаються

Функція не повертає значення після виконання.
