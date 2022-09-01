---
navigation:
  - class.swoole-event.html: « SwooleEvent
  - swoole-event.defer.html: 'SwooleEvent::defer »'
  - index.md: PHP Manual
  - class.swoole-event.html: SwooleEvent
title: 'SwooleEvent::add'
---
# SwooleEvent::add

(PECL swoole >= 1.9.0)

SwooleEvent::add - Додає нові callback-функції сокету в EventLoop

### Опис

```methodsynopsis
public static Swoole\Event::add(    int $fd,    callable $read_callback,    callable $write_callback = ?,    string $events = ?): bool
```

### Список параметрів

`fd`

`read_callback`

`write_callback`

`events`

### Значення, що повертаються
