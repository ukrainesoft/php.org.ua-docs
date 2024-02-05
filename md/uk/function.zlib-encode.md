---
navigation:
  - function.zlib-decode.md: « zlib\_decode
  - function.zlib-get-coding-type.md: zlib\_get\_coding\_type »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: zlib\_encode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zlib\_encode

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

zlib\_encode — Стиснення даних із зазначеним кодуванням

### Опис

```methodsynopsis
zlib_encode(string $data, int $encoding, int $level = -1): string|false
```

Стискає дані із зазначеним кодуванням.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`data`

Дані для стиснення.

`encoding`

Алгоритм сжатия. Одна из констант\*\*`ZLIB_ENCODING_RAW`\*\* **`ZLIB_ENCODING_DEFLATE`**или**`ZLIB_ENCODING_GZIP`**

`level`

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**zlib\_encode()\*\*\*\*

```php
<?php
$str = 'hello world';
$enc = zlib_encode($str, ZLIB_ENCODING_DEFLATE);
echo bin2hex($enc);
?>
```

Результат виконання наведеного прикладу:

```
789ccb48cdc9c95728cf2fca4901001a0b045d
```

### Дивіться також

-   [zlib\_decode()](function.zlib-decode.md) \- Розпаковує будь-які закодовані дані raw/gzip/zlib
