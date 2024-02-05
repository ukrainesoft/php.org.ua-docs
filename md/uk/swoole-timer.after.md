---
navigation:
  - class.swoole-timer.md: « Swoole\\Timer
  - swoole-timer.clear.md: 'Swoole\\Timer::clear »'
  - index.md: PHP Manual
  - class.swoole-timer.md: Swoole\\Timer
title: 'Swoole\\Timer::after'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Timer::after

(PECL swoole >= 1.9.0)

Swoole\\Timer::after - Запускає callback-функцію через певний проміжок часу

### Опис

```methodsynopsis
public static Swoole\Timer::after(int $after_time_ms, callable $callback): void
```

Запускає callback-функцію через певний проміжок часу.

### Список параметрів

`after_time_ms`

`callback`

### Значення, що повертаються
