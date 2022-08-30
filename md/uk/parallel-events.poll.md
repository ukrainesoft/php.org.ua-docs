Опитування

-   [« parallelEvents::remove](parallel-events.remove.html)
    
-   [parallelEventsInput »](class.parallel-events-input.html)
    
-   [PHP Manual](index.html)
    
-   [parallelEvents](class.parallel-events.html)
    
-   Опитування
    

# parallelEvents::poll

parallelEvents::poll — Опитування

### Опис

```methodsynopsis
public parallel\Events::poll(): ?parallel\Events\Event
```

Опитує для наступної події

### Значення, що повертаються

Якщо цілей не залишилося, повертається **`null`**

Якщо це буде неблокуючий цикл і відбудеться блокування, буде повернено значення **`null`**

В іншому випадку [parallelEventsEvent](class.parallel-events-event.html) повертає опис події.

### Помилки

**Увага**

Викидає parallelEventsErrorTimeout, якщо час очікування використано та досягнуто.