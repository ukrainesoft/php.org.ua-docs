Стиснути всі файли у поточному tar/zip-архіві

-   [« PharData::compress](phardata.compress.html)
    
-   [PharData::\_\_construct »](phardata.construct.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Стиснути всі файли у поточному tar/zip-архіві
    

# PharData::compressFiles

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::compressFiles — Стиснути всі файли у поточному tar/zip-архіві

### Опис

```methodsynopsis
public PharData::compressFiles(int $compression): void
```

Для tar-архівів цей метод викине виняток [BadMethodCallException](class.badmethodcallexception.html), оскільки стиснення окремих файлів у tar-архіві не підтримується форматом файлу. Використовуйте [PharData::compress()](phardata.compress.html) для стиснення всього tar-архіву.

Для Zip-архівів цей метод стисне всі файли, використовуючи заданий тип стиснення. Для коректної роботи потрібні включені модулі [zlib](ref.zlib.html) або [bzip2](ref.bzip2.html), Залежно від типу стиснення. Також, якщо деякі файли вже були стиснуті, необхідно, щоб відповідний модуль був включений, інакше не вдасться обробити.

### Список параметрів

`compression`

Одна з констант: `Phar::GZ` `Phar::BZ2` або `Phar::NONE`для скасування стиснення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.html) якщо вимкнено INI-опцію [phar.readonly](phar.configuration.html#ini.phar.readonly), якщо відсутній необхідний модуль [zlib](ref.zlib.html) або [bzip2](ref.bzip2.html)

### Приклади

**Приклад #1 Приклад використання **PharData::compressFiles()****

```php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar');
$p['myfile.txt'] = 'hi';
$p['myfile2.txt'] = 'hi';
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
$p->compressFiles(Phar::GZ);
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
?>
```

Результат виконання цього прикладу:

```
string(10) "myfile.txt"
bool(false)
bool(false)
bool(false)
string(11) "myfile2.txt"
bool(false)
bool(false)
bool(false)
string(10) "myfile.txt"
int(4096)
bool(false)
bool(true)
string(11) "myfile2.txt"
int(4096)
bool(false)
bool(true)
```

### Дивіться також

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.html) - Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.html) - Перевірити, чи стиснутий файл
-   [PharFileInfo::compress()](pharfileinfo.compress.html) - Стиснути поточний файл за допомогою zlib або bzip2
-   [PharFileInfo::decompress()](pharfileinfo.decompress.html) - Розтискає поточний файл
-   [Phar::canCompress()](phar.cancompress.html) - Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::isCompressed()](phar.iscompressed.html) - Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [PharData::decompressFiles()](phardata.decompressfiles.html) - Розпакувати всі файли у поточному zip-архіві
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.html) - Повертає масив підтримуваних алгоритмів стиснення
-   [PharData::compress()](phardata.compress.html) - Стискає весь архів tar/zip, використовуючи стиснення Gzip або Bzip2
-   [PharData::decompress()](phardata.decompress.html) - Розпакувати весь Phar-архів