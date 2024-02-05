---
navigation:
  - pharfileinfo.getcrc32.md: '« PharFileInfo::getCRC32'
  - pharfileinfo.getcontent.md: 'PharFileInfo::getContent »'
  - index.md: PHP Manual
  - class.pharfileinfo.md: PharFileInfo
title: 'PharFileInfo::getCompressedSize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharFileInfo::getCompressedSize

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

PharFileInfo::getCompressedSize — Отримати реальний розмір файлу на диску з урахуванням стиснення

### Опис

```methodsynopsis
public PharFileInfo::getCompressedSize(): int
```

Повертає реально займане файлом місце з урахуванням стиснення. Для стисненого файлу повернеться таке ж значення, що й за допомогою [filesize()](function.filesize.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Розмір файлу у байтах.

### Приклади

**Приклад #1 Приклад використання** PharFileInfo::getCompressedSize()\*\*\*\*

```php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    echo $file->getCompressedSize();
} catch (Exception $e) {
    echo 'Операции записи на my.phar завершились ошибкой: ', $e;
}
?>
```

Результат виконання наведеного прикладу:

```
2
```

### Дивіться також

-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.md) \- Перевірити, чи стиснутий файл
-   [PharFileInfo::decompress()](pharfileinfo.decompress.md) \- Розтискає поточний файл
-   [PharFileInfo::compress()](pharfileinfo.compress.md) \- Стиснути поточний файл за допомогою zlib або bzip2
-   [Phar::canCompress()](phar.cancompress.md) \- Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::isCompressed()](phar.iscompressed.md) \- Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [Phar::compress()](phar.compress.md) \- Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::decompress()](phar.decompress.md) \- Розпаковує весь Phar-архів
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.md) \- Повертає масив підтримуваних алгоритмів стиснення
-   [Phar::decompressFiles()](phar.decompressfiles.md) \- Розпаковує всі файли в поточному Phar-архіві
-   [Phar::compressFiles()](phar.compressfiles.md) \- Стискає всі файли у поточному Phar-архіві
