---
navigation:
  - swoole-server.addprocess.md: '« SwooleServer::addProcess'
  - swoole-server.bind.md: 'SwooleServer::bind »'
  - index.md: PHP Manual
  - class.swoole-server.md: SwooleServer
title: 'SwooleServer::after'
---
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
