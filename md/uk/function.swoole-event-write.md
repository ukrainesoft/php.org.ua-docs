---
navigation:
  - function.swoole-event-wait.md: « swoole\_event\_wait
  - function.swoole-get-local-ip.md: swoole\_get\_local\_ip »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_event\_write
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_event\_write

(PECL swoole >= 1.9.0)

swoole\_event\_write — Записати дані в сокет

### Опис

```methodsynopsis
swoole_event_write(int $fd, string $data): bool
```

### Список параметрів

`fd`

`data`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
