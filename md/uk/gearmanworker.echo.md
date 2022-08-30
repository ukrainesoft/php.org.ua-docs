Перевірка відгуку серверів завдань

-   [« GearmanWorker::construct](gearmanworker.construct.html)
    
-   [GearmanWorker::error »](gearmanworker.error.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanWorker](class.gearmanworker.html)
    
-   Перевірка відгуку серверів завдань
    

# GearmanWorker::echo

(PECL gearman >= 0.6.0)

GearmanWorker::echo — Перевірка відгуку серверів завдань

### Опис

```methodsynopsis
public GearmanWorker::echo(string $workload): bool
```

Надсилає дані всім серверам завдань, щоб перевірити, які із серверів дадуть відповідь. Це налагоджувальна функція для перевірки відгуку серверів.

### Список параметрів

`workload`

Довільні серіалізовані дані

### Значення, що повертаються

Стандартне для Gearman значення, що повертається.

### Дивіться також

-   [GearmanClient::echo()](gearmanclient.echo.html) - Надсилає дані всім серверам завдань, щоб перевірити відгук Застарілий метод