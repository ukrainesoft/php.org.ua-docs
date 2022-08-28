Додає нові callback функції сокету в EventLoop

-   [« Swoole\\Event](class.swoole-event.html)
    
-   [Swoole\\Event::defer »](swoole-event.defer.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole\\Event](class.swoole-event.html)
    
-   Додає нові callback функції сокету в EventLoop
    

# SwooleEvent::add

(PECL swoole >= 1.9.0)

SwooleEvent::add - Додає нові callback-функції сокету в EventLoop

### Опис

```methodsynopsis
public static Swoole\Event::add(    int $fd,    callable $read_callback,    callable $write_callback = ?,    string $events = ?): bool
```

### Список параметрів

`fd`

`read_callback`

`write_callback`

`events`

### Значення, що повертаються