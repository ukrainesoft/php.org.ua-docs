---
navigation:
  - function.zlib-decode.md: « zlibdecode
  - function.zlib-get-coding-type.md: zlibgetcodingtype »
  - index.md: PHP Manual
  - ref.zlib.md: Функции Zlib
title: zlibencode
---
# zlibencode

(PHP 5> = 5.4.0, PHP 7, PHP 8)

zlibencode — Стиснення даних із зазначеним кодуванням

### Опис

```methodsynopsis
zlib_encode(string $data, int $encoding, int $level = -1): string|false
```

Стискає дані із зазначеним кодуванням.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`data`

Дані для стиснення.

`encoding`

Алгоритм стискування. Одна з констант **`ZLIB_ENCODING_RAW`** **`ZLIB_ENCODING_DEFLATE`** або **`ZLIB_ENCODING_GZIP`**

`level`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **zlibencode()****

```php
<?php
$str = 'hello world';
$enc = zlib_encode($str, ZLIB_ENCODING_DEFLATE);
echo bin2hex($enc);
?>
```

Результат виконання цього прикладу:

```
789ccb48cdc9c95728cf2fca4901001a0b045d
```

### Дивіться також

-   [zlibdecode()](function.zlib-decode.md) - Розпаковує будь-які закодовані дані raw/gzip/zlib
