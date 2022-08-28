Додати нових callback-функцій сокету до циклу подій

-   [« swoole\_error\_log](function.swoole-error-log.html)
    
-   [swoole\_event\_defer »](function.swoole-event-defer.html)
    
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