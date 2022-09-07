---
navigation:
  - function.ltrim.md: « ltrim
  - function.md5.md: md5 »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: md5file
---
# md5file

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

md5file — Повертає MD5-хеш файлу

### Опис

```methodsynopsis
md5_file(string $filename, bool $binary = false): string|false
```

Обчислює MD5-хеш файлу, ім'я якого задано аргументом `filename`, використовуючи [» алгоритм MD5 RSA Data Security, Inc.](http://www.faqs.org/rfcs/rfc1321) і повертає цей хеш. Хеш є 32-значним шістнадцятковим числом.

### Список параметрів

`filename`

ім'я файлу

`binary`

Якщо має значення **`true`**, то повертається бінарний рядок із 16 символів.

### Значення, що повертаються

Повертає рядок у разі успішного виконання, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **md5file()****

```php
<?php
$file = 'php-5.3.0alpha2-Win32-VC9-x64.zip';

echo 'MD5-хеш файла ' . $file . ': ' . md5_file($file);
?>
```

### Дивіться також

-   [md5()](function.md5.md) - Повертає MD5-хеш рядки
-   [sha1file()](function.sha1-file.md) - Повертає SHA1-хеш файлу
-   [crc32()](function.crc32.md) - Обчислює поліном CRC32 для рядка
