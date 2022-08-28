Запускає callback-функцію після закінчення певного періоду часу

-   [« Swoole\\Server::addProcess](swoole-server.addprocess.html)
    
-   [Swoole\\Server::bind »](swoole-server.bind.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole\\Server](class.swoole-server.html)
    
-   Запускає callback-функцію після закінчення певного періоду часу
    

# SwooleServer::after

(PECL swoole >= 1.9.0)

SwooleServer::after — Запускає callback-функцію після закінчення певного періоду часу

### Опис

```methodsynopsis
public Swoole\Server::after(int $after_time_ms, callable $callback, string $param = ?): ReturnType
```

### Список параметрів

`after_time_ms`

`callback`

`param`

### Значення, що повертаються