Встановлює мінімальну кількість паралельних потоків

-   [« eio\_set\_max\_poll\_time](function.eio-set-max-poll-time.html)
    
-   [eio\_stat »](function.eio-stat.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Встановлює мінімальну кількість паралельних потоків
    

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

-   [eio\_nthreads()](function.eio-nthreads.html) - Повертає кількість потоків, що використовуються в даний момент
-   [eio\_set\_max\_idle()](function.eio-set-max-idle.html) - Встановлює максимальну кількість очікуваних потоків
-   [eio\_set\_max\_parallel()](function.eio-set-max-parallel.html) - Встановлює максимальну кількість паралельних потоків