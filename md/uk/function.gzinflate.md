---
navigation:
  - function.gzgetss.md: « gzgetss
  - function.gzopen.md: gzopen »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gzinflate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gzinflate

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gzinflate — Розпакувати стислий рядок

### Опис

```methodsynopsis
gzinflate(string $data, int $max_length = 0): string|false
```

Розпаковує стислий рядок.

### Список параметрів

`data`

Дані, стислі функцією [gzdeflate()](function.gzdeflate.md)

`max_length`

Максимальний розмір даних, що декодуються.

### Значення, що повертаються

Розпаковані дані або \*\*`false`\*\*в случае возникновения ошибки.

Функція поверне помилку, якщо стиснуті дані в 32768 разів більше розміру стислих даних `data` або, якщо `max_length`не і більше, ніж необов'язковий параметр `max_length`

### Приклади

**Пример #1 Пример использования**gzinflate()\*\*\*\*

```php
<?php
$compressed   = gzdeflate('Сожми меня', 9);
$uncompressed = gzinflate($compressed);
echo $uncompressed;
?>
```

### Дивіться також

-   [gzdeflate()](function.gzdeflate.md) \- Стискає рядок
-   [gzcompress()](function.gzcompress.md) \- Стиснути рядок
-   [gzuncompress()](function.gzuncompress.md) \- Розпакувати стислий рядок
-   [gzencode()](function.gzencode.md) \- Створити стислий рядок gzip
