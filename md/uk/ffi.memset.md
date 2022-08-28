Заповнити область пам'яті

-   [« FFI::memcpy](ffi.memcpy.html)
    
-   [FFI::new »](ffi.new.html)
    
-   [PHP Manual](index.html)
    
-   [FFI](class.ffi.html)
    
-   Заповнити область пам'яті
    

# FFI::memset

(PHP 7> = 7.4.0, PHP 8)

FFI::memset — Заповнити область пам'яті

### Опис

```methodsynopsis
public static FFI::memset(FFI\CData &$ptr, int $value, int $size): void
```

Заповнює `size` байт пам'яті за вказівником `ptr` значенням `value`

### Список параметрів

`ptr`

Вказівник початку ділянки пам'яті.

`value`

Значення заповнення.

`size`

Кількість байт, які будуть заповнені.

### Значення, що повертаються

Функція не повертає значення після виконання.