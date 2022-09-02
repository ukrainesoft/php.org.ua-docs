---
navigation:
  - swoole-server.bind.md: '« SwooleServer::bind'
  - swoole-server.close.md: 'SwooleServer::close »'
  - index.md: PHP Manual
  - class.swoole-server.md: SwooleServer
title: 'SwooleServer::clearTimer'
---
# SwooleServer::clearTimer

# swooletimerclear

(PECL swoole >= 1.9.0)

SwooleServer::clearTimer -- swooletimerclear — Зупиняє та знищує таймер

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Swoole\Server::clearTimer(int $timer_id): void
```

Процедурний стиль:

```methodsynopsis
swoole_timer_clear(int $timer_id): void
```

Зупиняє та знищує таймер

### Список параметрів

`timer_id`

### Значення, що повертаються
