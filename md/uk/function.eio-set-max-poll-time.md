Встановлює максимальний час виконання

-   [« eio\_set\_max\_poll\_reqs](function.eio-set-max-poll-reqs.html)
    
-   [eio\_set\_min\_parallel »](function.eio-set-min-parallel.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Встановлює максимальний час виконання
    

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