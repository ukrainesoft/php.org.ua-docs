Припинення

-   [« parallel\\Future](class.parallel-future.html)
    
-   [parallel\\Future::cancelled »](parallel-future.cancelled.html)
    
-   [PHP Manual](index.html)
    
-   [parallel\\Future](class.parallel-future.html)
    
-   Припинення
    

# parallelFuture::cancel

parallelFuture::cancel — Припинення

### Опис

```methodsynopsis
public parallel\Future::cancel(): bool
```

Намагається перервати завдання.

> **Зауваження**
> 
> Якщо завдання запущено, його буде перервано.

**Увага**

Внутрішні виклики функцій не можуть бути перервані.

### Винятки

**Увага**

Викидає parallelFutureErrorKilled, якщо [parallel\\Runtime](class.parallel-runtime.html) виконання завдання було перервано.

**Увага**

Викидає parallelFutureErrorCancelled, якщо завдання вже перервано.