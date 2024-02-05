---
navigation:
  - phar.buildfromiterator.md: '« Phar::buildFromIterator'
  - phar.canwrite.md: 'Phar::canWrite »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::canCompress'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Може бути використана одна з констант `Phar::GZ`или`Phar::BZ2` для перевірки можливості стиснення алгоритму zlib або bzip2 відповідно.

### Значення, що повертаються

**`true`**, якщо стиснення/розпакування доступні, **`false`**, в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** Phar::canCompress()\*\*\*\*

```php
<?php
if (Phar::canCompress()) {
    echo file_get_contents('phar://compressedphar.phar/internal/file.txt');
} else {
    echo 'сжатие недоступно';
}
?>
```

### Дивіться також

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.md) \- Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.md) \- Перевірити, чи стиснутий файл
-   [PharFileInfo::compress()](pharfileinfo.compress.md) \- Стиснути поточний файл за допомогою zlib або bzip2
-   [PharFileInfo::decompress()](pharfileinfo.decompress.md) \- Розтискає поточний файл
-   [Phar::isCompressed()](phar.iscompressed.md) \- Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [Phar::compressFiles()](phar.compressfiles.md) \- Стискає всі файли у поточному Phar-архіві
-   [Phar::decompressFiles()](phar.decompressfiles.md) \- Розпаковує всі файли в поточному Phar-архіві
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.md) \- Повертає масив підтримуваних алгоритмів стиснення
-   [Phar::convertToExecutable()](phar.converttoexecutable.md) \- Конвертує phar-архів в інший формат файлу, що виконується.
-   [Phar::convertToData()](phar.converttodata.md) \- Конвертує phar-архів в tar-або zip-файл, що не виконується.
