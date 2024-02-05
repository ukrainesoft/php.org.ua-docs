---
navigation:
  - function.eio-nop.md: « eio\_nop
  - function.eio-nready.md: eio\_nready »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_npending
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_npending

(PECL eio >= 0.0.1dev)

eio\_npending — Повертає кількість завершених, але необроблених процесів

### Опис

```methodsynopsis
eio_npending(): int
```

**eio\_npending()** повертає кількість завершених, але необроблених процесів

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**eio\_npending()** повертає кількість завершених, але необроблених процесів.

### Дивіться також

-   [eio\_nreqs()](function.eio-nreqs.md) \- Повертає кількість запитів, які потрібно виконати
-   [eio\_nready()](function.eio-nready.md) \- Повертає кількість ще не опрацьованих запитів
-   [eio\_nthreads()](function.eio-nthreads.md) \- Повертає кількість потоків, що використовуються в даний момент
