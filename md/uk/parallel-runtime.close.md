Витончене з'єднання під час виконання

-   [« parallel\\Runtime::run](parallel-runtime.run.html)
    
-   [parallel\\Runtime::kill »](parallel-runtime.kill.html)
    
-   [PHP Manual](index.html)
    
-   [parallel\\Runtime](class.parallel-runtime.html)
    
-   Витончене з'єднання під час виконання
    

# parallelRuntime::close

parallelRuntime::close — Витончене з'єднання під час виконання

### Опис

```methodsynopsis
public parallel\Runtime::close(): void
```

Запитує завершення роботи середовища виконання.

> **Зауваження**
> 
> Заплановані для виконання завдання будуть виконані до завершення роботи.

### Помилки

**Увага**

Викидає parallelRuntimeErrorClosed, якщо Runtime вже було закрито.