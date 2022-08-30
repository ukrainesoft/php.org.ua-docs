Повертає розмір даних або типу C

-   [« FFI::scope](ffi.scope.html)
    
-   [FFI::string »](ffi.string.html)
    
-   [PHP Manual](index.html)
    
-   [FFI](class.ffi.html)
    
-   Повертає розмір даних або типу C
    

# FFI::sizeof

(PHP 7> = 7.4.0, PHP 8)

FFI::sizeof — Повертає розмір даних або типу C

### Опис

```methodsynopsis
public static FFI::sizeof(FFI\CData|FFI\CType &$ptr): int
```

Повертає розмір об'єктів [FFICData](class.ffi-cdata.html) або [FFICType](class.ffi-ctype.html)

### Список параметрів

`ptr`

Дескриптор покажчика на тип чи дані C.

### Значення, що повертаються

Розмір області пам'яті, який вказує `ptr`