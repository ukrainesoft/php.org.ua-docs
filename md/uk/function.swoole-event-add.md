---
navigation:
  - function.swoole-error-log.md: « swoole\_error\_log
  - function.swoole-event-defer.md: swoole\_event\_defer »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_event\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_event\_add

(PECL swoole >= 1.9.0)

swoole\_event\_add — Додати нових callback-функцій сокету до циклу подій

### Опис

```methodsynopsis
swoole_event_add(    int $fd,    callable $read_callback = ?,    callable $write_callback = ?,    int $events = 0): int
```

### Список параметрів

`fd`

`read_callback`

`write_callback`

`events`

### Значення, що повертаються
