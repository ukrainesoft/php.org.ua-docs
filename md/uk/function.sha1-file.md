---
navigation:
  - function.setlocale.md: « setlocale
  - function.sha1.md: sha1 »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: sha1\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sha1\_file

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

sha1\_file — Повертає SHA1-хеш файлу

### Опис

```methodsynopsis
sha1_file(string $filename, bool $binary = false): string|false
```

Обчислює SHA1-хеш файлу, ім'я якого задано аргументом `filename`, используя алгоритм[» US Secure Hash Algorithm 1](http://www.faqs.org/rfcs/rfc3174) і повертає цей хеш. Хеш – 40-символьне шістнадцяткове число.

### Список параметрів

`filename`

Ім'я файлу, що хешується.

`binary`

Если установлен в\*\*`true`\*\*, повертає 20-символьний хеш у бінарному форматі

### Значення, що повертаються

Повертає рядок у разі успішного виконання, інакше повертається **`false`**

### Приклади

**Пример #1 Пример использования**sha1\_file()\*\*\*\*

```php
<?php
foreach(glob('/home/Kalle/myproject/*.php') as $ent)
{
    if(is_dir($ent))
    {
        continue;
    }

    echo $ent . ' (SHA1: ' . sha1_file($ent) . ')', PHP_EOL;
}
?>
```

### Дивіться також

-   [sha1()](function.sha1.md) \- Повертає SHA1-хеш рядки
-   [md5\_file()](function.md5-file.md) \- Повертає MD5-хеш файлу
-   [crc32()](function.crc32.md) \- Обчислює поліном CRC32 для рядка
