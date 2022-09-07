---
navigation:
  - function.swoole-errno.md: « swooleerrno
  - function.swoole-event-add.md: swooleeventadd »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функции Swoole
title: swooleerrorlog
---
# swooleerrorlog

(PECL swoole >= 4.5.8)

swooleerrorlog — Виводить повідомлення про помилки до журналу

### Опис

```methodsynopsis
swoole_error_log(int $level, string $msg): void
```

Виводить повідомлення про помилки до журналу.

### Список параметрів

`level`

Рівень запису в журнал можна використовувати константи: **`SWOOLE_LOG_DEBUG`** **`SWOOLE_LOG_TRACE`** **`SWOOLE_LOG_INFO`** **`SWOOLE_LOG_NOTICE`** **`SWOOLE_LOG_WARNING`** **`SWOOLE_LOG_ERROR`** **`SWOOLE_LOG_NONE`**

`msg`

Повідомлення, яке записується в журнал.

### Значення, що повертаються

Функція не повертає значення після виконання.
