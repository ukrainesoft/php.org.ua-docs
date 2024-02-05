---
navigation:
  - function.swoole-clear-error.md: « swoole\_clear\_error
  - function.swoole-cpu-num.md: swoole\_cpu\_num »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_client\_select
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_client\_select

(PECL swoole >= 1.9.0)

swoole\_client\_select — Отримати опис файлу, готового до читання/запису або помилки

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
