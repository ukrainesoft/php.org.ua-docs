Повертає спосіб кодування, який використовується для стиснення виводу

-   [« zlibencode](function.zlib-encode.html)
    
-   [DeflateContext »](class.deflatecontext.md)
    
-   [PHP Manual](index.md)
    
-   [Функции Zlib](ref.zlib.md)
    
-   Повертає спосіб кодування, який використовується для стиснення виводу
    

# zlibgetcodingtype

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

zlibgetcodingtype — Повертає спосіб кодування, який використовується для стиснення виводу.

### Опис

```methodsynopsis
zlib_get_coding_type(): string|false
```

Повертає спосіб кодування, який використовується для стиснення виводу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Можливі значення: `gzip` `deflate` або **`false`**

### Дивіться також

-   Директива [zlib.outputcompression](zlib.configuration.html#ini.zlib.output-compression)