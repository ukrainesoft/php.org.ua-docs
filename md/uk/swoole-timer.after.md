---
navigation:
  - class.swoole-timer.md: « SwooleTimer
  - swoole-timer.clear.md: 'SwooleTimer::clear »'
  - index.md: PHP Manual
  - class.swoole-timer.md: SwooleTimer
title: 'SwooleTimer::after'
---
# SwooleTimer::after

(PECL swoole >= 1.9.0)

SwooleTimer::after - Запускає callback-функцію через певний проміжок часу

### Опис

```methodsynopsis
public static Swoole\Timer::after(int $after_time_ms, callable $callback): void
```

Запускає callback-функцію через певний проміжок часу.

### Список параметрів

`after_time_ms`

`callback`

### Значення, що повертаються
