---
navigation:
  - function.gzclose.md: « gzclose
  - function.gzdecode.md: gzdecode »
  - index.md: PHP Manual
  - ref.zlib.md: Функции Zlib
title: gzcompress
---
# gzcompress

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

gzcompress — Стиснути рядок

### Опис

```methodsynopsis
gzcompress(string $data, int $level = -1, int $encoding = ZLIB_ENCODING_DEFLATE): string|false
```

Ця функція стискає рядок, використовуючи формат даних `ZLIB`

Детальніше про алгоритм стиснення ZLIB дивіться документ "[» Формат стиснення ZLIB. Специфікація версії 3.3](http://www.faqs.org/rfcs/rfc1950)(RFC 1950).

> **Зауваження**
> 
> Це *не* те ж саме, що і gzip-стиск, який включає деякі дані заголовка. Інформацію про gzip-стиснення дивіться [gzencode()](function.gzencode.md)

### Список параметрів

`data`

Дані для стиснення.

`level`

Рівень стиску. Ціле число від 0 до 9 (0 – без стиску, 9 – максимальне стиск).

Якщо використовується значення -1, то буде встановлено прийнятий у бібліотеці zlib за умовчанням рівень стиснення, що дорівнює 6.

`encoding`

Одна з констант **`ZLIB_ENCODING_*`**

### Значення, що повертаються

Стиснутий рядок або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **gzcompress()****

```php
<?php
$compressed = gzcompress('Сожми меня', 9);
echo $compressed;
?>
```

### Дивіться також

-   [gzdeflate()](function.gzdeflate.md) - Стискає рядок
-   [gzinflate()](function.gzinflate.md) - Розпакувати стислий рядок
-   [gzuncompress()](function.gzuncompress.md) - Розпакувати стислий рядок
-   [gzencode()](function.gzencode.md) - Створити стислий рядок gzip
