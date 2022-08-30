Прив'язує callback-функцію до HTTP-сервера на ім'я події

-   [« SwooleHttpServer](class.swoole-http-server.html)
    
-   [SwooleHttpServer::start »](swoole-http-server.start.html)
    
-   [PHP Manual](index.md)
    
-   [SwooleHttpServer](class.swoole-http-server.html)
    
-   Прив'язує callback-функцію до HTTP-сервера на ім'я події
    

# SwooleHttpServer::on

(PECL swoole >= 1.9.0)

SwooleHttpServer::on — Прив'язує callback-функцію до HTTP-сервера на ім'я події

### Опис

```methodsynopsis
public Swoole\Http\Server::on(string $event_name, callable $callback): void
```

Прив'язує callback-функцію до HTTP-сервера на ім'я події.

### Список параметрів

`event_name`

`callback`

### Значення, що повертаються