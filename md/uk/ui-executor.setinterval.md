Управління інтервалом

-   [« UIExecutor::onExecute](ui-executor.onexecute.html)
    
-   [ОЙControlsTab »](class.ui-controls-tab.html)
    
-   [PHP Manual](index.html)
    
-   [ОЙExecutor](class.ui-executor.html)
    
-   Управління інтервалом
    

# ОЙExecutor::setInterval

(UI 2.0.0)

ОЙExecutor::setInterval — Керування інтервалом

### Опис

```methodsynopsis
public UI\Executor::setInterval(int $microseconds): bool
```

```methodsynopsis
public UI\Executor::setInterval(int $seconds, int $microseconds): bool
```

Встановить новий інтервал. Інтервал 0 припиняє виконання виконавцем доти, доки не буде встановлено новий інтервал

### Список параметрів

`seconds`

`microseconds`

### Значення, що повертаються

Індикатор успішності виконання