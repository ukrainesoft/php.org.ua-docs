---
navigation:
  - ffi.type.md: '« FFI::type'
  - class.ffi-cdata.md: FFI\\CData »
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::typeof'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FFI::typeof

(PHP 7 >= 7.4.0, PHP 8)

FFI::typeof — Отримує FFI\\CType для FFI\\CData

### Опис

```methodsynopsis
public static FFI::typeof(FFI\CData &$ptr): FFI\CType
```

Повертає об'єкт [FFI\\CType](class.ffi-ctype.md), що представляє тип об'єкта [FFI\\CData](class.ffi-cdata.md)

### Список параметрів

`ptr`

Вказівник на структуру даних C.

### Значення, що повертаються

Повертає об'єкт [FFI\\CType](class.ffi-ctype.md), що представляє тип об'єкта [FFI\\CData](class.ffi-cdata.md)
