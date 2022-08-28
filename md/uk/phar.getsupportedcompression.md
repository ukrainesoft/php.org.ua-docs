Повертає масив підтримуваних алгоритмів стиснення

-   [« Phar::getStub](phar.getstub.html)
    
-   [Phar::getSupportedSignatures »](phar.getsupportedsignatures.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Повертає масив підтримуваних алгоритмів стиснення
    

# Phar::getSupportedCompression

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.2.0)

Phar::getSupportedCompression — Повертає масив підтримуваних алгоритмів стиснення

### Опис

```methodsynopsis
final public static Phar::getSupportedCompression(): array
```

### Список параметрів

Немає параметрів.

### Значення, що повертаються

Повертає масив, що містить будь-які значення `Phar::GZ` або `Phar::BZ2` залежно від доступності модулів [zlib](book.zlib.html) і [bz2](book.bzip2.html)

### Дивіться також

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.html) - Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.html) - Перевірити, чи стиснутий файл
-   [PharFileInfo::compress()](pharfileinfo.compress.html) - Стиснути поточний файл за допомогою zlib або bzip2
-   [PharFileInfo::decompress()](pharfileinfo.decompress.html) - Розтискає поточний файл
-   [Phar::compress()](phar.compress.html) - Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::decompress()](phar.decompress.html) - Розпаковує весь Phar-архів
-   [Phar::canCompress()](phar.cancompress.html) - Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::isCompressed()](phar.iscompressed.html) - Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [Phar::compressFiles()](phar.compressfiles.html) - Стискає всі файли у поточному Phar-архіві
-   [Phar::decompressFiles()](phar.decompressfiles.html) - Розпаковує всі файли в поточному Phar-архіві