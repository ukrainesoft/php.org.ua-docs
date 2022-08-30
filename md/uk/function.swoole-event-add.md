Додати нових callback-функцій сокету до циклу подій

-   [« swooleerrorlog](function.swoole-error-log.html)
    
-   [swooleeventdefer »](function.swoole-event-defer.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Swoole](ref.swoole-funcs.html)
    
-   Додати нових callback-функцій сокету до циклу подій
    

# swooleeventadd

(PECL swoole >= 1.9.0)

swooleeventadd — Додати нових callback-функцій сокету до циклу подій

### Опис

```methodsynopsis
swoole_event_add(    int $fd,    callable $read_callback = ?,    callable $write_callback = ?,    int $events = 0): int
```

### Список параметрів

`fd`

`read_callback`

`write_callback`

`events`

### Значення, що повертаються