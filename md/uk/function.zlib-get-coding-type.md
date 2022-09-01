---
navigation:
  - function.zlib-encode.html: « zlibencode
  - class.deflatecontext.md: DeflateContext »
  - index.md: PHP Manual
  - ref.zlib.md: Функции Zlib
title: zlibgetcodingtype
---
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
