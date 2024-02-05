---
navigation:
  - function.gztell.md: « gztell
  - function.gzwrite.md: gzwrite »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gzuncompress
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gzuncompress

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

gzuncompress — Розпакувати стислий рядок

### Опис

```methodsynopsis
gzuncompress(string $data, int $max_length = 0): string|false
```

Розпаковує стислий рядок.

### Список параметрів

`data`

Дані, стислі функцією [gzcompress()](function.gzcompress.md)

`max_length`

Максимальний розмір даних декодування.

### Значення, що повертаються

Вихідні несжаті дані або \*\*`false`\*\*в случае возникновения ошибки.

Функція також повідомить про помилку у випадку, якщо стиснуті дані в 32768 разів більше розміру стислих даних `data`или больше параметра`max_length`

### Приклади

**Приклад #1 Приклад використання** gzuncompress()\*\*\*\*

```php
<?php
$compressed   = gzcompress('Сожми меня', 9);
$uncompressed = gzuncompress($compressed);
echo $uncompressed;
?>
```

### Дивіться також

-   [gzcompress()](function.gzcompress.md) \- Стиснути рядок
-   [gzinflate()](function.gzinflate.md) \- Розпакувати стислий рядок
-   [gzdeflate()](function.gzdeflate.md) \- Стискає рядок
-   [gzencode()](function.gzencode.md) \- Створити стислий рядок gzip
