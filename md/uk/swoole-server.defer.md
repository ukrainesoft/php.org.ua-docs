---
navigation:
  - swoole-server.construct.md: '« SwooleServer::construct'
  - swoole-server-port.construct.md: 'SwooleServerPort::construct »'
  - index.md: PHP Manual
  - class.swoole-server.md: SwooleServer
title: 'SwooleServer::defer'
---
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
