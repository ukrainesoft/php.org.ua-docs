---
navigation:
  - function.swoole-event-add.md: « swoole\_event\_add
  - function.swoole-event-del.md: swoole\_event\_del »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_event\_defer
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_event\_defer

(PECL swoole >= 1.9.0)

swoole\_event\_defer — Додати callback-функцію до наступного циклу подій

### Опис

```methodsynopsis
swoole_event_defer(callable $callback): bool
```

### Список параметрів

`callback`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
