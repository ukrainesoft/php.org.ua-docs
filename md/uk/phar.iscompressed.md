Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)

-   [« Phar::isBuffering](phar.isbuffering.html)
    
-   [Phar::isFileFormat »](phar.isfileformat.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
    

# Phar::isCompressed

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::isCompressed — Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)

### Опис

```methodsynopsis
public Phar::isCompressed(): int|false
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.html) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.html)

Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі). Phar-архіви, засновані на zip, не можуть бути стиснуті цілком, тому цей метод завжди повертає **`false`**якщо він був викликаний на phar-архіві, заснованому на zip.

### Список параметрів

Немає параметрів.

### Значення, що повертаються

`Phar::GZ` `Phar::BZ2` або **`false`**

### Приклади

**Приклад #1 Приклад використання **Phar::isCompressed()****

```php
<?php
try {
    $phar1 = new Phar('myphar.zip.phar');
    var_dump($phar1->isCompressed());
    $phar2 = new Phar('myuncompressed.tar.phar');
    var_dump($phar2->isCompressed());
    $phar2->compress(Phar::GZ);
    var_dump($phar2->isCompressed() == Phar::GZ);
} catch (Exception $e) {
}
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(false)
bool(true)
```

### Дивіться також

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.html) - Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.html) - Перевірити, чи стиснутий файл
-   [PharFileInfo::decompress()](pharfileinfo.decompress.html) - Розтискає поточний файл
-   [PharFileInfo::compress()](pharfileinfo.compress.html) - Стиснути поточний файл за допомогою zlib або bzip2
-   [Phar::decompress()](phar.decompress.html) - Розпаковує весь Phar-архів
-   [Phar::compress()](phar.compress.html) - Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::canCompress()](phar.cancompress.html) - Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::compressFiles()](phar.compressfiles.html) - Стискає всі файли в поточному Phar-архіві
-   [Phar::decompressFiles()](phar.decompressfiles.html) - Розпаковує всі файли в поточному Phar-архіві
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.html) - Повертає масив підтримуваних алгоритмів стиснення