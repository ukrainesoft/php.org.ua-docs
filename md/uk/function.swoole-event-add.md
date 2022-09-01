---
navigation:
  - function.swoole-error-log.html: « swooleerrorlog
  - function.swoole-event-defer.html: swooleeventdefer »
  - index.html: PHP Manual
  - ref.swoole-funcs.html: Функции Swoole
title: swooleeventadd
---
# swooleeventadd

(PECL swoole >= 1.9.0)

swooleeventadd — Додати нових callback-функцій сокету до циклу подій

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
