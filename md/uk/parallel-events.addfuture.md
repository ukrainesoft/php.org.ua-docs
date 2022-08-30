Цілі

-   [« parallelEvents::addChannel](parallel-events.addchannel.html)
    
-   [parallelEvents::remove »](parallel-events.remove.html)
    
-   [PHP Manual](index.html)
    
-   [parallelEvents](class.parallel-events.html)
    
-   Цілі
    

# parallelEvents::addFuture

parallelEvents::addFuture — Цілі

### Опис

```methodsynopsis
public parallel\Events::addFuture(string $name, parallel\Future $future): void
```

Стежить за подіями у заданому `future`

### Помилки

**Увага**

Викидає parallelEventsErrorExistence, якщо ціль з даним ім'ям вже був доданий.