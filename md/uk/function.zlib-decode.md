---
navigation:
  - function.readgzfile.md: « readgzfile
  - function.zlib-encode.md: zlibencode »
  - index.md: PHP Manual
  - ref.zlib.md: Функции Zlib
title: zlibdecode
---
# zlibdecode

(PHP 5> = 5.4.0, PHP 7, PHP 8)

zlibdecode — Розпаковує будь-які закодовані дані raw/gzip/zlib

### Опис

```methodsynopsis
zlib_decode(string $data, int $max_length = 0): string|false
```

Розпаковує будь-які закодовані дані raw/gzip/zlib.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`data`

`max_length`

### Значення, що повертаються

Повертає розпаковані дані або **`false`** у разі виникнення помилки.

### Дивіться також

-   [zlibencode()](function.zlib-encode.md) - Стиснення даних із зазначеним кодуванням
