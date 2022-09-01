---
navigation:
  - function.swoole-clear-error.html: « swooleclearerror
  - function.swoole-cpu-num.html: swoolecpunum »
  - index.html: PHP Manual
  - ref.swoole-funcs.html: Функции Swoole
title: swooleclientselect
---
# swooleclientselect

(PECL swoole >= 1.9.0)

swooleclientselect — Отримати опис файлу, готового до читання/запису або помилки

### Опис

```methodsynopsis
swoole_client_select(    array &$read_array,    array &$write_array,    array &$error_array,    float $timeout = 0.5): int
```

### Список параметрів

`read_array`

`write_array`

`error_array`

`timeout`

### Значення, що повертаються
