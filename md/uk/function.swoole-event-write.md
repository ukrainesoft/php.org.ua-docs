---
navigation:
  - function.swoole-event-wait.html: « swooleeventwait
  - function.swoole-get-local-ip.html: swoolegetlocalip »
  - index.md: PHP Manual
  - ref.swoole-funcs.html: Функции Swoole
title: swooleeventwrite
---
# swooleeventwrite

(PECL swoole >= 1.9.0)

swooleeventwrite — Записати дані в сокет

### Опис

```methodsynopsis
swoole_event_write(int $fd, string $data): bool
```

### Список параметрів

`fd`

`data`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
