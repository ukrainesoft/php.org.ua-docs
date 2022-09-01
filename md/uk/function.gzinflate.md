---
navigation:
  - function.gzgetss.html: « gzgetss
  - function.gzopen.html: gzopen »
  - index.html: PHP Manual
  - ref.zlib.html: Функции Zlib
title: gzinflate
---
# gzinflate

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gzinflate — Розпакувати стислий рядок

### Опис

```methodsynopsis
gzinflate(string $data, int $max_length = 0): string|false
```

Розпаковує стислий рядок.

### Список параметрів

`data`

Дані, стислі функцією [gzdeflate()](function.gzdeflate.html)

`max_length`

Максимальний розмір даних, що декодуються.

### Значення, що повертаються

Розпаковані дані або **`false`** у разі виникнення помилки.

Функція поверне помилку, якщо стиснуті дані в 32768 разів більше розміру стислих даних `data` або, якщо `max_length` не `0` і більше, ніж необов'язковий параметр `max_length`

### Приклади

**Приклад #1 Приклад використання **gzinflate()****

```php
<?php
$compressed   = gzdeflate('Сожми меня', 9);
$uncompressed = gzinflate($compressed);
echo $uncompressed;
?>
```

### Дивіться також

-   [gzdeflate()](function.gzdeflate.html) - Стискає рядок
-   [gzcompress()](function.gzcompress.html) - Стиснути рядок
-   [gzuncompress()](function.gzuncompress.html) - Розпакувати стислий рядок
-   [gzencode()](function.gzencode.html) - Створити стислий рядок gzip
