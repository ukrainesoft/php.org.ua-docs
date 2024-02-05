---
navigation:
  - ffi.addr.md: '« FFI::addr'
  - ffi.arraytype.md: 'FFI::arrayType »'
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::alignof'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FFI::alignof

(PHP 7 >= 7.4.0, PHP 8)

FFI::alignof — Повертає величину вирівнювання

### Опис

```methodsynopsis
public static FFI::alignof(FFI\CData|FFI\CType &$ptr): int
```

Повертає величину вирівнювання об'єктів [FFI\\CData](class.ffi-cdata.md) або [FFI\\CType](class.ffi-ctype.md)

### Список параметрів

`ptr`

Дескриптор покажчика даних або тип C.

### Значення, що повертаються

Повертає величину вирівнювання об'єктів [FFI\\CData](class.ffi-cdata.md) або [FFI\\CType](class.ffi-ctype.md)
