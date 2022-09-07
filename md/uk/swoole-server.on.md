---
navigation:
  - swoole-server.listen.md: '« SwooleServer::listen'
  - swoole-server.pause.md: 'SwooleServer::pause »'
  - index.md: PHP Manual
  - class.swoole-server.md: SwooleServer
title: 'SwooleServer::on'
---
# SwooleServer::on

(PECL swoole >= 1.9.0)

SwooleServer::on — Реєструє callback-функцію на ім'я події

### Опис

```methodsynopsis
public Swoole\Server::on(string $event_name, callable $callback): void
```

### Список параметрів

`event_name`

`callback`

### Значення, що повертаються
