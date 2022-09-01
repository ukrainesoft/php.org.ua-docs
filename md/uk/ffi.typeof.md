---
navigation:
  - ffi.type.md: '« FFI::type'
  - class.ffi-cdata.html: FFICData »
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::typeof'
---
# FFI::typeof

(PHP 7> = 7.4.0, PHP 8)

FFI::typeof — Отримує FFICType для FFICData

### Опис

```methodsynopsis
public static FFI::typeof(FFI\CData &$ptr): FFI\CType
```

Повертає об'єкт [FFICType](class.ffi-ctype.html), що представляє тип об'єкта [FFICData](class.ffi-cdata.md)

### Список параметрів

`ptr`

Вказівник на структуру даних C.

### Значення, що повертаються

Повертає об'єкт [FFICType](class.ffi-ctype.html), що представляє тип об'єкта [FFICData](class.ffi-cdata.md)
