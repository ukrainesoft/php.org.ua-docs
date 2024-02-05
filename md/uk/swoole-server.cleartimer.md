---
navigation:
  - swoole-server.bind.md: '« Swoole\\Server::bind'
  - swoole-server.close.md: 'Swoole\\Server::close »'
  - index.md: PHP Manual
  - class.swoole-server.md: Swoole\\Server
title: 'Swoole\\Server::clearTimer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Server::clearTimer

# swoole\_timer\_clear

(PECL swoole >= 1.9.0)

Swoole\\Server::clearTimer -- swoole\_timer\_clear — Зупиняє та знищує таймер

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
