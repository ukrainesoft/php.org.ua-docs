Отримує FFICType для FFICData

-   [« FFI::type](ffi.type.html)
    
-   [FFI\\CData »](class.ffi-cdata.html)
    
-   [PHP Manual](index.html)
    
-   [FFI](class.ffi.html)
    
-   Отримує FFICType для FFICData
    

# FFI::typeof

(PHP 7> = 7.4.0, PHP 8)

FFI::typeof — Отримує FFICType для FFICData

### Опис

```methodsynopsis
public static FFI::typeof(FFI\CData &$ptr): FFI\CType
```

Повертає об'єкт [FFI\\CType](class.ffi-ctype.html), що представляє тип об'єкта [FFI\\CData](class.ffi-cdata.html)

### Список параметрів

`ptr`

Вказівник на структуру даних C.

### Значення, що повертаються

Повертає об'єкт [FFI\\CType](class.ffi-ctype.html), що представляє тип об'єкта [FFI\\CData](class.ffi-cdata.html)