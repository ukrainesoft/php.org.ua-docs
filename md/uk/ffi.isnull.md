---
navigation:
  - ffi.free.md: '« FFI::free'
  - ffi.load.md: 'FFI::load »'
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::isNull'
---
# FFI::isNull

(PHP 7> = 7.4.0, PHP 8)

FFI::isNull — Перевіряє, чи є FFICData нульовим покажчиком

### Опис

```methodsynopsis
public static FFI::isNull(FFI\CData &$ptr): bool
```

Перевіряє, чи є FFICData є нульовим покажчиком.

### Список параметрів

`ptr`

Вказівник на структуру даних C.

### Значення, що повертаються

Повертає **`true`** або **`false`** залежно від того, чи є FFICData є нульовим покажчиком.
