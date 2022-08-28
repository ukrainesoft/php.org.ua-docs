Комплексний приклад PHP/FFI/preloading

-   [« Callback-функции PHP](ffi.examples-callback.html)
    
-   [FFI »](class.ffi.html)
    
-   [PHP Manual](index.html)
    
-   [Примеры](ffi.examples.html)
    
-   Комплексний приклад PHP/FFI/preloading
    

## Комплексний приклад PHP/FFI/preloading

php.ini

ffi.enable=preload opcache.preload=preload.php

preload.php

```php
<?php
FFI::load(__DIR__ . "/dummy.h");
opcache_compile_file(__DIR__ . "/dummy.php");
?>
```

dummy.h

#define FFISCOPE "DUMMY" #define FFILIB "libc.so.6"

int printf(const char format, ...);

dummy.php

```php
<?php
final class Dummy {
    private static $ffi = null;
    function __construct() {
        if (is_null(self::$ffi)) {
            self::$ffi = FFI::scope("DUMMY");
        }
    }
    function printf($format, ...$args) {
       return (int)self::$ffi->printf($format, ...$args);
    }
}
?>
```

test.php

```php
<?php
$d = new Dummy();
$d->printf("Привет, %s!\n", "мир");
?>
```