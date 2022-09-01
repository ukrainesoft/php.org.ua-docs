---
navigation:
  - ffi.addr.html: '« FFI::addr'
  - ffi.arraytype.html: 'FFI::arrayType »'
  - index.html: PHP Manual
  - class.ffi.html: FFI
title: 'FFI::alignof'
---
# FFI::alignof

(PHP 7> = 7.4.0, PHP 8)

FFI::alignof — Повертає величину вирівнювання

### Опис

```methodsynopsis
public static FFI::alignof(FFI\CData|FFI\CType &$ptr): int
```

Повертає величину вирівнювання об'єктів [FFICData](class.ffi-cdata.html) або [FFICType](class.ffi-ctype.html)

### Список параметрів

`ptr`

Дескриптор покажчика даних або тип C.

### Значення, що повертаються

Повертає величину вирівнювання об'єктів [FFICData](class.ffi-cdata.html) або [FFICType](class.ffi-ctype.html)
