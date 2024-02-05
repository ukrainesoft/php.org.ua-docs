---
navigation:
  - ffi.scope.md: '« FFI::scope'
  - ffi.string.md: 'FFI::string »'
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::sizeof'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FFI::sizeof

(PHP 7 >= 7.4.0, PHP 8)

FFI::sizeof — Повертає розмір даних або типу C

### Опис

```methodsynopsis
public static FFI::sizeof(FFI\CData|FFI\CType &$ptr): int
```

Повертає розмір об'єктів [FFI\\CData](class.ffi-cdata.md) або [FFI\\CType](class.ffi-ctype.md)

### Список параметрів

`ptr`

Дескриптор покажчика на тип чи дані C.

### Значення, що повертаються

Розмір області пам'яті, який вказує `ptr`
