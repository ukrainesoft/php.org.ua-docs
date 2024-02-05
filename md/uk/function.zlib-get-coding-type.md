---
navigation:
  - function.zlib-encode.md: « zlib\_encode
  - class.deflatecontext.md: DeflateContext »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: zlib\_get\_coding\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zlib\_get\_coding\_type

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

zlib\_get\_coding\_type — Повертає спосіб кодування, який використовується для стиснення виводу.

### Опис

```methodsynopsis
zlib_get_coding_type(): string|false
```

Повертає спосіб кодування, який використовується для стиснення виведення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Можливі значення: `gzip` `deflate`или\*\*`false`\*\*

### Дивіться також

-   Директива[zlib.output\_compression](zlib.configuration.md#ini.zlib.output-compression)
