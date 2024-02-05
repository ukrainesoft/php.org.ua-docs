---
navigation:
  - class.swoole-event.md: « Swoole\\Event
  - swoole-event.defer.md: 'Swoole\\Event::defer »'
  - index.md: PHP Manual
  - class.swoole-event.md: Swoole\\Event
title: 'Swoole\\Event::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Event::add

(PECL swoole >= 1.9.0)

Swoole\\Event::add - Додає нові callback-функції сокету в EventLoop

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
