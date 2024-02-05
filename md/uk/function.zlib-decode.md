---
navigation:
  - function.readgzfile.md: « readgzfile
  - function.zlib-encode.md: zlib\_encode »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: zlib\_decode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zlib\_decode

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

zlib\_decode — Розпаковує будь-які закодовані дані raw/gzip/zlib

### Опис

```methodsynopsis
zlib_decode(string $data, int $max_length = 0): string|false
```

Розпаковує будь-які закодовані дані raw/gzip/zlib.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`data`

`max_length`

### Значення, що повертаються

Повертає розпаковані дані або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [zlib\_encode()](function.zlib-encode.md) \- Стиснення даних із зазначеним кодуванням
