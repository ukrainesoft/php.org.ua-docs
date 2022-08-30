Конструктор класу

-   [« parallelSync](class.parallel-sync.html)
    
-   [parallelSync::get »](parallel-sync.get.html)
    
-   [PHP Manual](index.html)
    
-   [parallelSync](class.parallel-sync.html)
    
-   Конструктор класу
    

# parallelSync::construct

parallelSync::construct - Конструктор класу

### Опис

```methodsynopsis
public parallel\Sync::__construct()
```

Створює новий об'єкт синхронізації без значення.

```methodsynopsis
public parallel\Sync::__construct(scalar $value)
```

Створює новий об'єкт синхронізації, який містить задане скалярне значення.

### Помилки

**Увага**

Викидає parallelSyncErrorIlegallegalValue, якщо `value` не є скалярним значенням.