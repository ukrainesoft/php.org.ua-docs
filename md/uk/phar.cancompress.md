---
navigation:
  - phar.buildfromiterator.html: '« Phar::buildFromIterator'
  - phar.canwrite.html: 'Phar::canWrite »'
  - index.html: PHP Manual
  - class.phar.html: Phar
title: 'Phar::canCompress'
---
# Phar::canCompress

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::canCompress — Перевіряє, чи модуль phar підтримує стиснення з використанням zlib або bzip2

### Опис

```methodsynopsis
final public static Phar::canCompress(int $compression = 0): bool
```

Цей метод слід використовувати для перевірки підтримки стиснення до завантаження phar-архіву, що містить стислі файли.

### Список параметрів

`compression`

Може бути використана одна з констант `Phar::GZ` або `Phar::BZ2` для перевірки можливості стиснення алгоритму zlib або bzip2 відповідно.

### Значення, що повертаються

**`true`**, якщо стиснення/розпакування доступні, **`false`**, в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **Phar::canCompress()****

```php
<?php
if (Phar::canCompress()) {
    echo file_get_contents('phar://compressedphar.phar/internal/file.txt');
} else {
    echo 'сжатие недоступно';
}
?>
```

### Дивіться також

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.html) - Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.html) - Перевірити, чи стиснутий файл
-   [PharFileInfo::compress()](pharfileinfo.compress.html) - Стиснути поточний файл за допомогою zlib або bzip2
-   [PharFileInfo::decompress()](pharfileinfo.decompress.html) - Розтискає поточний файл
-   [Phar::isCompressed()](phar.iscompressed.html) - Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [Phar::compressFiles()](phar.compressfiles.html) - Стискає всі файли в поточному Phar-архіві
-   [Phar::decompressFiles()](phar.decompressfiles.html) - Розпаковує всі файли в поточному Phar-архіві
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.html) - Повертає масив підтримуваних алгоритмів стиснення
-   [Phar::convertToExecutable()](phar.converttoexecutable.html) - Конвертує phar-архів в інший формат файлу, що виконується.
-   [Phar::convertToData()](phar.converttodata.html) - Конвертує phar-архів в tar-або zip-файл, що не виконується.
