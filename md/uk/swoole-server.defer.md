Відкладає виконання callback-функції наприкінці поточного EventLoop

-   [« SwooleServer::construct](swoole-server.construct.html)
    
-   [SwooleServerPort::construct »](swoole-server-port.construct.html)
    
-   [PHP Manual](index.html)
    
-   [SwooleServer](class.swoole-server.html)
    
-   Відкладає виконання callback-функції наприкінці поточного EventLoop
    

# SwooleServer::defer

(PECL swoole >= 1.9.0)

SwooleServer::defer — Відкладає виконання callback-функції в кінці поточного EventLoop

### Опис

```methodsynopsis
public Swoole\Server::defer(callable $callback): void
```

### Список параметрів

`callback`

### Значення, що повертаються