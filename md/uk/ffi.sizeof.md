---
navigation:
  - ffi.scope.md: '« FFI::scope'
  - ffi.string.md: 'FFI::string »'
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::sizeof'
---
# FFI::sizeof

(PHP 7> = 7.4.0, PHP 8)

FFI::sizeof — Повертає розмір даних або типу C

### Опис

```methodsynopsis
public static FFI::sizeof(FFI\CData|FFI\CType &$ptr): int
```

Повертає розмір об'єктів [FFICData](class.ffi-cdata.html) або [FFICType](class.ffi-ctype.md)

### Список параметрів

`ptr`

Дескриптор покажчика на тип чи дані C.

### Значення, що повертаються

Розмір області пам'яті, який вказує `ptr`
