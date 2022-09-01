---
navigation:
  - function.swoole-event-add.html: « swooleeventadd
  - function.swoole-event-del.html: swooleeventdel »
  - index.html: PHP Manual
  - ref.swoole-funcs.html: Функции Swoole
title: swooleeventdefer
---
# swooleeventdefer

(PECL swoole >= 1.9.0)

swooleeventdefer — Додати callback-функцію до наступного циклу подій

### Опис

```methodsynopsis
swoole_event_defer(callable $callback): bool
```

### Список параметрів

`callback`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
