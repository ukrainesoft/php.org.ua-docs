---
navigation:
  - function.swoole-event-exit.html: « swooleeventexit
  - function.swoole-event-wait.html: swooleeventwait »
  - index.md: PHP Manual
  - ref.swoole-funcs.html: Функции Swoole
title: swooleeventset
---
# swooleeventset

(PECL swoole >= 1.9.0)

swooleeventset - Оновити callback-функції події сокету

### Опис

```methodsynopsis
swoole_event_set(    int $fd,    callable $read_callback = ?,    callable $write_callback = ?,    int $events = 0): bool
```

### Список параметрів

`fd`

`read_callback`

`write_callback`

`events`

### Значення, що повертаються
