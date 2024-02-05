---
navigation:
  - function.swoole-event-defer.md: « swoole\_event\_defer
  - function.swoole-event-exit.md: swoole\_event\_exit »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_event\_del
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_event\_del

(PECL swoole >= 1.9.0)

swoole\_event\_del — Видалити всі callback функції сокету

### Опис

```methodsynopsis
swoole_event_del(int $fd): bool
```

### Список параметрів

`fd`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
