Встановлює мінімальну кількість паралельних потоків

-   [« eiosetmaxpolltime](function.eio-set-max-poll-time.html)
    
-   [eiostat »](function.eio-stat.html)
    
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

-   [eionthreads()](function.eio-nthreads.html) - Повертає кількість потоків, що використовуються в даний момент
-   [eiosetmaxidle()](function.eio-set-max-idle.html) - Встановлює максимальну кількість очікуваних потоків
-   [eiosetmaxparallel()](function.eio-set-max-parallel.html) - Встановлює максимальну кількість паралельних потоків