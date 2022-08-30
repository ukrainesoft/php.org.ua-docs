З'єднання під час виконання

-   [« parallelRuntime::close](parallel-runtime.close.html)
    
-   [parallelFuture »](class.parallel-future.html)
    
-   [PHP Manual](index.html)
    
-   [parallelRuntime](class.parallel-runtime.html)
    
-   З'єднання під час виконання
    

# parallelRuntime::kill

parallelRuntime::kill — З'єднання під час виконання

### Опис

```methodsynopsis
public parallel\Runtime::kill(): void
```

Намагається примусово завершити роботу середовища виконання.

> **Зауваження**
> 
> Заплановані для виконання завдання не будуть виконані, поточне завдання буде перервано.

**Увага**

Внутрішні виклики функцій не можуть бути перервані.

### Помилки

**Увага**

Викидає parallelRuntimeErrorClosed, якщо Runtime вже було закрито.