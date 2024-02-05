---
navigation:
  - function.swoole-event-exit.md: « swoole\_event\_exit
  - function.swoole-event-wait.md: swoole\_event\_wait »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_event\_set
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_event\_set

(PECL swoole >= 1.9.0)

swoole\_event\_set - Оновити callback-функції події сокету

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
