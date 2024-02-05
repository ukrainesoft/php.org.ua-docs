---
navigation:
  - function.gzdeflate.md: « gzdeflate
  - function.gzeof.md: gzeof »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gzencode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gzencode

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gzencode — Створити стислий рядок gzip

### Опис

```methodsynopsis
gzencode(string $data, int $level = -1, int $encoding = ZLIB_ENCODING_GZIP): string|false
```

Ця функція повертає стислу версію вхідних даних `data`, аналогічно висновку програми **gzip**

Подробности о формате GZIP смотрите[» Формат файлу GZIP. Специфікація версії 4.3](http://www.faqs.org/rfcs/rfc1952)(RFC 1952).

### Список параметрів

`data`

Дані кодування.

`level`

Рівень стиску. 0 – без стиску, 9 – максимальне стиск. Якщо не вказано, використовуватиметься рівень стиснення за замовчуванням бібліотеки zlib.

`encoding`

Режим стиснення, можливо **`FORCE_GZIP`**(по умолчанию) или\*\*`FORCE_DEFLATE`\*\*

Використання константи **`FORCE_DEFLATE`** генерує висновок, сумісний з RFC 1950, що складається із заголовка zlib, стислих даних та контрольної суми Adler.

### Значення, що повертаються

Сжатая строка или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

Повертаються дані будуть містити відповідні заголовки та структури даних як у звичайному .gz-файлі, наприклад:

**Приклад #1 Створення файлу gzip**

```php
<?php
$data = file_get_contents("bigfile.txt");
$gzdata = gzencode($data, 9);
file_put_contents("bigfile.txt.gz", $gzdata);
?>
```

### Дивіться також

-   [gzdecode()](function.gzdecode.md) \- Декодує рядок, стислий за допомогою gzip
-   [gzdeflate()](function.gzdeflate.md) \- Стискає рядок
-   [gzinflate()](function.gzinflate.md) \- Розпакувати стислий рядок
-   [gzuncompress()](function.gzuncompress.md) \- Розпакувати стислий рядок
-   [gzcompress()](function.gzcompress.md) \- Стиснути рядок
-   [»  Специфікація ZLIB Compressed Data (RFC 1950)](http://www.faqs.org/rfcs/rfc1950)
