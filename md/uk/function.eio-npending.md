---
navigation:
  - function.eio-nop.html: « eionop
  - function.eio-nready.html: eionready »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eionpending
---
# eionpending

(PECL eio >= 0.0.1dev)

eionpending — Повертає кількість завершених, але необроблених процесів

### Опис

```methodsynopsis
eio_npending(): int
```

**eionpending()** повертає кількість завершених, але необроблених процесів

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**eionpending()** повертає кількість завершених, але необроблених процесів.

### Дивіться також

-   [eionreqs()](function.eio-nreqs.md) - Повертає кількість запитів, які потрібно виконати
-   [eionready()](function.eio-nready.md) - Повертає кількість ще не опрацьованих запитів
-   [eionthreads()](function.eio-nthreads.md) - Повертає кількість потоків, що використовуються в даний момент
