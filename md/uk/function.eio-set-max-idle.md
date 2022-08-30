Встановлює максимальну кількість очікуваних потоків

-   [« eiosendfile](function.eio-sendfile.html)
    
-   [eiosetmaxparallel »](function.eio-set-max-parallel.html)
    
-   [PHP Manual](index.md)
    
-   [Eio Функции](ref.eio.md)
    
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

-   [eionthreads()](function.eio-nthreads.html) - Повертає кількість потоків, що використовуються в даний момент
-   [eiosetminparallel()](function.eio-set-min-parallel.html) - Встановлює мінімальну кількість паралельних потоків
-   [eiosetmaxparallel()](function.eio-set-max-parallel.html) - Встановлює максимальну кількість паралельних потоків