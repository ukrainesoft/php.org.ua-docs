Доступ

-   [« parallelSync::get](parallel-sync.get.html)
    
-   [parallelSync::wait »](parallel-sync.wait.html)
    
-   [PHP Manual](index.html)
    
-   [parallelSync](class.parallel-sync.html)
    
-   Доступ
    

# parallelSync::set

parallelSync::set — Доступ

### Опис

```methodsynopsis
public parallel\Sync::set(scalar $value)
```

Атомарно встановлює значення синхронізації об'єкта.

### Помилки

**Увага**

Викидає parallelSyncErrorIlegallegalValue, якщо `value` не є скалярним значенням.