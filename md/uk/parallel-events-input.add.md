Входи

-   [« parallelEventsInput](class.parallel-events-input.html)
    
-   [parallelEventsInput::clear »](parallel-events-input.clear.html)
    
-   [PHP Manual](index.html)
    
-   [parallelEventsInput](class.parallel-events-input.html)
    
-   Входи
    

# parallelEventsInput::add

parallelEventsInput::add — Вхід

### Опис

```methodsynopsis
public parallel\Events\Input::add(string $target, mixed $value): void
```

Встановлює вхід для заданої мети

### Помилки

**Увага**

Викидає parallelEventsInputErrorExistence, якщо вхід до мети вже існує.

**Увага**

Викидає parallelEventsInputErrorIllegalValue, якщо значення неприпустимо (object, **`null`**