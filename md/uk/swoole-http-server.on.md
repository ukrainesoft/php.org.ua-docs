---
navigation:
  - class.swoole-http-server.md: « Swoole\\Http\\Server
  - swoole-http-server.start.md: 'Swoole\\Http\\Server::start »'
  - index.md: PHP Manual
  - class.swoole-http-server.md: Swoole\\Http\\Server
title: 'Swoole\\Http\\Server::on'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Http\\Server::on

(PECL swoole >= 1.9.0)

Swoole\\Http\\Server::on — Прив'язує callback-функцію до HTTP-сервера на ім'я події

### Опис

```methodsynopsis
public Swoole\Http\Server::on(string $event_name, callable $callback): void
```

Прив'язує callback-функцію до HTTP-сервера на ім'я події.

### Список параметрів

`event_name`

`callback`

### Значення, що повертаються
