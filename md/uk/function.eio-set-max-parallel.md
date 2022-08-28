Встановлює максимальну кількість паралельних потоків

-   [« eio\_set\_max\_idle](function.eio-set-max-idle.html)
    
-   [eio\_set\_max\_poll\_reqs »](function.eio-set-max-poll-reqs.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Встановлює максимальну кількість паралельних потоків
    

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

-   [eio\_nthreads()](function.eio-nthreads.html) - Повертає кількість потоків, що використовуються в даний момент
-   [eio\_set\_max\_idle()](function.eio-set-max-idle.html) - Встановлює максимальну кількість очікуваних потоків
-   [eio\_set\_min\_parallel()](function.eio-set-min-parallel.html) - Встановлює мінімальну кількість паралельних потоків