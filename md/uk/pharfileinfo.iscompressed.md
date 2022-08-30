Перевірити, чи стиснений файл

-   [« PharFileInfo::isCRCChecked](pharfileinfo.iscrcchecked.md)
    
-   [PharFileInfo::setMetadata »](pharfileinfo.setmetadata.md)
    
-   [PHP Manual](index.md)
    
-   [PharFileInfo](class.pharfileinfo.md)
    
-   Перевірити, чи стиснений файл
    

# PharFileInfo::isCompressed

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

PharFileInfo::isCompressed — Перевірити, чи стиснений файл

### Опис

```methodsynopsis
public PharFileInfo::isCompressed(?int $compression = null): bool
```

Перевіряє, чи стиснений файл усередині Phar-архіву за допомогою Gzip або Bzip2.

### Список параметрів

`compression`

Одна з констант **`Phar::GZ`** або **`Phar::BZ2`**. За замовчуванням – будь-який тип стиснення.

### Значення, що повертаються

**`true`**, якщо файл стиснутий і **`false`** в іншому випадку.

### список змін

| Версия | Описание |
| --- | --- |
|  | `compression` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::isCompressed()****

```php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $p['myfile2.txt'] = 'hi';
    $p['myfile2.txt']->setCompressedGZ();
    $file = $p['myfile.txt'];
    $file2 = $p['myfile2.txt'];
    var_dump($file->isCompressed());
    var_dump($file2->isCompressed());
} catch (Exception $e) {
    echo 'Не удалось создать/изменить phar my.phar: ', $e;
}
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.md) - Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::decompress()](pharfileinfo.decompress.md) - Розтискає поточний файл
-   [PharFileInfo::compress()](pharfileinfo.compress.md) - Стиснути поточний файл за допомогою zlib або bzip2
-   [Phar::decompress()](phar.decompress.md) - Розпаковує весь Phar-архів
-   [Phar::compress()](phar.compress.md) - Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::canCompress()](phar.cancompress.md) - Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::isCompressed()](phar.iscompressed.md) - Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.md) - Повертає масив підтримуваних алгоритмів стиснення
-   [Phar::decompressFiles()](phar.decompressfiles.md) - Розпаковує всі файли в поточному Phar-архіві
-   [Phar::compressFiles()](phar.compressfiles.md) - Стискає всі файли у поточному Phar-архіві