Встановлює максимальну кількість очікуваних потоків

-   [« eio\_sendfile](function.eio-sendfile.html)
    
-   [eio\_set\_max\_parallel »](function.eio-set-max-parallel.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Встановлює максимальну кількість очікуваних потоків
    

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

-   [eio\_nthreads()](function.eio-nthreads.html) - Повертає кількість потоків, що використовуються в даний момент
-   [eio\_set\_min\_parallel()](function.eio-set-min-parallel.html) - Встановлює мінімальну кількість паралельних потоків
-   [eio\_set\_max\_parallel()](function.eio-set-max-parallel.html) - Встановлює максимальну кількість паралельних потоків