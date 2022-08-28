Отримати реальний розмір файлу на диску з урахуванням стиснення

-   [« PharFileInfo::getCRC32](pharfileinfo.getcrc32.html)
    
-   [PharFileInfo::getContent »](pharfileinfo.getcontent.html)
    
-   [PHP Manual](index.html)
    
-   [PharFileInfo](class.pharfileinfo.html)
    
-   Отримати реальний розмір файлу на диску з урахуванням стиснення
    

# PharFileInfo::getCompressedSize

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

PharFileInfo::getCompressedSize — Отримати реальний розмір файлу на диску з урахуванням стиснення

### Опис

```methodsynopsis
public PharFileInfo::getCompressedSize(): int
```

Повертає реально займане файлом місце з урахуванням стиснення. Для стисненого файлу повернеться таке ж значення, що й за допомогою [filesize()](function.filesize.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Розмір файлу у байтах.

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::getCompressedSize()****

```php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    echo $file->getCompressedSize();
} catch (Exception $e) {
    echo 'Операции записи на my.phar завершились ошибкой: ', $e;
}
?>
```

Результат виконання цього прикладу:

```
2
```

### Дивіться також

-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.html) - Перевірити, чи стиснутий файл
-   [PharFileInfo::decompress()](pharfileinfo.decompress.html) - Розтискає поточний файл
-   [PharFileInfo::compress()](pharfileinfo.compress.html) - Стиснути поточний файл за допомогою zlib або bzip2
-   [Phar::canCompress()](phar.cancompress.html) - Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::isCompressed()](phar.iscompressed.html) - Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [Phar::compress()](phar.compress.html) - Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::decompress()](phar.decompress.html) - Розпаковує весь Phar-архів
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.html) - Повертає масив підтримуваних алгоритмів стиснення
-   [Phar::decompressFiles()](phar.decompressfiles.html) - Розпаковує всі файли в поточному Phar-архіві
-   [Phar::compressFiles()](phar.compressfiles.html) - Стискає всі файли в поточному Phar-архіві