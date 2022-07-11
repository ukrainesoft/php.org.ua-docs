- [« Callback-функції PHP](ffi.examples-callback.md)
- [FFI »](class.ffi.md)

- [PHP Manual](index.md)
- [Приклади](ffi.examples.md)
- Комплексний приклад PHP/FFI/preloading

## Комплексний приклад PHP/FFI/preloading

`php.ini`

`` inicode
ffi.enable=preload
opcache.preload=preload.php
````

`preload.php`

` <?phpFFI::load(__DIR__ . "/dummy.h");opcache_compile_file(__DIR__ . "/dummy.php");?> `

`dummy.h`

`` ccode
#define FFI_SCOPE "DUMMY"
#define FFI_LIB "libc.so.6"

int printf(const char *format, ...);
````

`dummy.php`

`<?phpfinal class Dummy {     private static $ffi = null; function __construct() {        if (is_null(self::$ffi)) {            selsel::$ffi = FFI::scope("DUMMY" }    }    function printf($format, ...$args) {      return (int)self::$ffi->printf($format, ...$args); }}?> `

`test.php`

` <?php$d = new Dummy();$d->printf("Привіт,%s!"
", "світ");?> `
