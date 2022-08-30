Створює некерований покажчик даних C

-   [« FFI](class.ffi.html)
    
-   [FFI::alignof »](ffi.alignof.html)
    
-   [PHP Manual](index.html)
    
-   [FFI](class.ffi.html)
    
-   Створює некерований покажчик даних C
    

# FFI::addr

(PHP 7> = 7.4.0, PHP 8)

FFI::addr — Створює некерований покажчик даних C

### Опис

```methodsynopsis
public static FFI::addr(FFI\CData &$ptr): FFI\CData
```

Створює некерований покажчик даних C, представлені заданим [FFICData](class.ffi-cdata.html). Початковий `ptr` повинен пережити результуючий покажчик. Ця функція використовується головним чином передачі аргументів в функцію C за покажчиком.

### Список параметрів

`ptr`

Дескриптор некерованого покажчика структуру даних.

### Значення, що повертаються

Повертає новий об'єкт [FFICData](class.ffi-cdata.html)