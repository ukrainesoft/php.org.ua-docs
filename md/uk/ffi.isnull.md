Перевіряє, чи є FFICData нульовим покажчиком

-   [« FFI::free](ffi.free.html)
    
-   [FFI::load »](ffi.load.html)
    
-   [PHP Manual](index.html)
    
-   [FFI](class.ffi.html)
    
-   Перевіряє, чи є FFICData нульовим покажчиком
    

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