---
navigation:
  - function.swoole-load-module.html: « swooleloadmodule
  - function.swoole-set-process-name.html: swoolesetprocessname »
  - index.html: PHP Manual
  - ref.swoole-funcs.html: Функции Swoole
title: swooleselect
---
# swooleselect

(PECL swoole >= 1.9.0)

swooleselect — Вибрати опис файлів, які готові до читання/запису або помилки в цикл подій

### Опис

```methodsynopsis
swoole_select(    array &$read_array,    array &$write_array,    array &$error_array,    float $timeout = ?): int
```

### Список параметрів

`read_array`

`write_array`

`error_array`

`timeout`

### Значення, що повертаються
