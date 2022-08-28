Повертає кількість потоків, що використовуються в даний момент

-   [« eio\_nreqs](function.eio-nreqs.html)
    
-   [eio\_open »](function.eio-open.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Повертає кількість потоків, що використовуються в даний момент
    

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

-   [eio\_npending()](function.eio-npending.html) - Повертає кількість завершених, але необроблених процесів
-   [eio\_nready()](function.eio-nready.html) - Повертає кількість ще не опрацьованих запитів
-   [eio\_nreqs()](function.eio-nreqs.html) - Повертає кількість запитів, які потрібно виконати
-   [eio\_set\_max\_idle()](function.eio-set-max-idle.html) - Встановлює максимальну кількість очікуваних потоків
-   [eio\_set\_max\_parallel()](function.eio-set-max-parallel.html) - Встановлює максимальну кількість паралельних потоків
-   [eio\_set\_min\_parallel()](function.eio-set-min-parallel.html) - Встановлює мінімальну кількість паралельних потоків