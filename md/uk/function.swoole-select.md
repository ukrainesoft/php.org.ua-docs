---
navigation:
  - function.swoole-load-module.md: « swoole\_load\_module
  - function.swoole-set-process-name.md: swoole\_set\_process\_name »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_select
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_select

(PECL swoole >= 1.9.0)

swoole\_select — Вибрати опис файлів, які готові до читання/запису або помилки в цикл подій

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
