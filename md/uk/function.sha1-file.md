Повертає SHA1-хеш файлу

-   [« setlocale](function.setlocale.html)
    
-   [sha1 »](function.sha1.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Повертає SHA1-хеш файлу
    

# sha1file

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

sha1file — Повертає SHA1-хеш файлу

### Опис

```methodsynopsis
sha1_file(string $filename, bool $binary = false): string|false
```

Обчислює SHA1-хеш файлу, ім'я якого задано аргументом `filename`, використовуючи алгоритм [» US Secure Hash Algorithm 1](http://www.faqs.org/rfcs/rfc3174) і повертає цей хеш. Хеш – 40-символьне шістнадцяткове число.

### Список параметрів

`filename`

Ім'я файлу, що хешується.

`binary`

Якщо встановлений у **`true`**, повертає 20-символьний хеш у бінарному форматі

### Значення, що повертаються

Повертає рядок у разі успішного виконання, інакше повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **sha1file()****

```php
<?php
foreach(glob('/home/Kalle/myproject/*.php') as $ent)
{
    if(is_dir($ent))
    {
        continue;
    }

    echo $ent . ' (SHA1: ' . sha1_file($ent) . ')', PHP_EOL;
}
?>
```

### Дивіться також

-   [sha1()](function.sha1.html) - Повертає SHA1-хеш рядки
-   [md5\_file()](function.md5-file.html) - Повертає MD5-хеш файлу
-   [crc32()](function.crc32.html) - Обчислює поліном CRC32 для рядка