Запускає callback-функцію через певний проміжок часу

-   [« SwooleTimer](class.swoole-timer.html)
    
-   [SwooleTimer::clear »](swoole-timer.clear.html)
    
-   [PHP Manual](index.html)
    
-   [SwooleTimer](class.swoole-timer.html)
    
-   Запускає callback-функцію через певний проміжок часу
    

# SwooleTimer::after

(PECL swoole >= 1.9.0)

SwooleTimer::after - Запускає callback-функцію через певний проміжок часу

### Опис

```methodsynopsis
public static Swoole\Timer::after(int $after_time_ms, callable $callback): void
```

Запускає callback-функцію через певний проміжок часу.

### Список параметрів

`after_time_ms`

`callback`

### Значення, що повертаються