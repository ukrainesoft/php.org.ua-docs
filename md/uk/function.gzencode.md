Створити стислий рядок gzip

-   [« gzdeflate](function.gzdeflate.md)
    
-   [gzeof »](function.gzeof.md)
    
-   [PHP Manual](index.md)
    
-   [Функции Zlib](ref.zlib.md)
    
-   Створити стислий рядок gzip
    

# gzencode

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gzencode — Створити стислий рядок gzip

### Опис

```methodsynopsis
gzencode(string $data, int $level = -1, int $encoding = ZLIB_ENCODING_GZIP): string|false
```

Ця функція повертає стислу версію вхідних даних `data`, аналогічно висновку програми **gzip**

Подробиці про формат GZIP дивіться [» Формат файлу GZIP. Специфікація версії 4.3](http://www.faqs.org/rfcs/rfc1952) (RFC 1952).

### Список параметрів

`data`

Дані кодування.

`level`

Рівень стиску. 0 – без стиску, 9 – максимальне стиск. Якщо не вказано, використовуватиметься рівень стиснення за замовчуванням бібліотеки zlib.

`encoding`

Режим стиснення, можливо **`FORCE_GZIP`** (за замовчуванням) або **`FORCE_DEFLATE`**

Використання константи **`FORCE_DEFLATE`** генерує висновок, сумісний з RFC 1950, що складається із заголовка zlib, стислих даних та контрольної суми Adler.

### Значення, що повертаються

Стиснутий рядок або **`false`** у разі виникнення помилки.

### Приклади

Повертаються дані будуть містити відповідні заголовки та структури даних як у звичайному .gz-файлі, наприклад:

**Приклад #1 Створення файлу gzip**

```php
<?php
$data = file_get_contents("bigfile.txt");
$gzdata = gzencode($data, 9);
file_put_contents("bigfile.txt.gz", $gzdata);
?>
```

### Дивіться також

-   [gzdecode()](function.gzdecode.md) - Декодує рядок, стислий за допомогою gzip
-   [gzdeflate()](function.gzdeflate.md) - Стискає рядок
-   [gzinflate()](function.gzinflate.md) - Розпакувати стислий рядок
-   [gzuncompress()](function.gzuncompress.md) - Розпакувати стислий рядок
-   [gzcompress()](function.gzcompress.md) - Стиснути рядок
-   [»  Спецификация ZLIB Compressed Data (RFC 1950)](http://www.faqs.org/rfcs/rfc1950)