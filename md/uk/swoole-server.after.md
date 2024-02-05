---
navigation:
  - swoole-server.addprocess.md: '« Swoole\\Server::addProcess'
  - swoole-server.bind.md: 'Swoole\\Server::bind »'
  - index.md: PHP Manual
  - class.swoole-server.md: Swoole\\Server
title: 'Swoole\\Server::after'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Server::after

(PECL swoole >= 1.9.0)

Swoole\\Server::after — Запускає callback-функцію після закінчення певного періоду часу

### Опис

```methodsynopsis
public Swoole\Server::after(int $after_time_ms, callable $callback, string $param = ?): ReturnType
```

### Список параметрів

`after_time_ms`

`callback`

`param`

### Значення, що повертаються
