---
navigation:
  - function.swoole-errno.md: « swoole\_errno
  - function.swoole-event-add.md: swoole\_event\_add »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_error\_log
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_error\_log

(PECL swoole >= 4.5.8)

swoole\_error\_log — Виводить повідомлення про помилки до журналу

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
