---
navigation:
  - class.swoole-http-server.md: « SwooleHttpServer
  - swoole-http-server.start.md: 'SwooleHttpServer::start »'
  - index.md: PHP Manual
  - class.swoole-http-server.md: SwooleHttpServer
title: 'SwooleHttpServer::on'
---
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
