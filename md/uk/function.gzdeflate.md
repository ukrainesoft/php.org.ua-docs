---
navigation:
  - function.gzdecode.md: « gzdecode
  - function.gzencode.md: gzencode »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gzdeflate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gzdeflate

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gzdeflate — Стискає рядок

### Опис

```methodsynopsis
gzdeflate(string $data, int $level = -1, int $encoding = ZLIB_ENCODING_RAW): string|false
```

Ця функція стискає рядок, використовуючи формат даних `DEFLATE`

Детальніше про алгоритм стиснення DEFLATE дивіться "[» Формат стиснення даних DEFLATE. Специфікація версії 1.3](http://www.faqs.org/rfcs/rfc1951)" (RFC 1951).

### Список параметрів

`data`

Дані для стиснення.

`level`

Рівень стиску. 0 – без стиску, 9 – максимум. Якщо не вказано, використовуватиметься рівень стиснення за замовчуванням бібліотеки zlib.

`encoding`

Одна из\*\*`ZLIB_ENCODING_*`\*\*констант.

### Значення, що повертаються

Сжатая строка или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** gzdeflate()\*\*\*\*

```php
<?php
$compressed = gzdeflate('Сожми меня', 9);
echo $compressed;
?>
```

### Дивіться також

-   [gzinflate()](function.gzinflate.md) \- Розпакувати стислий рядок
-   [gzcompress()](function.gzcompress.md) \- Стиснути рядок
-   [gzuncompress()](function.gzuncompress.md) \- Розпакувати стислий рядок
-   [gzencode()](function.gzencode.md) \- Створити стислий рядок gzip
