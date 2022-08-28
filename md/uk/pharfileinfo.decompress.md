Розтискає поточний файл

-   [« PharFileInfo::\_\_construct](pharfileinfo.construct.html)
    
-   [PharFileInfo::delMetadata »](pharfileinfo.delmetadata.html)
    
-   [PHP Manual](index.html)
    
-   [PharFileInfo](class.pharfileinfo.html)
    
-   Розтискає поточний файл
    

# PharFileInfo::decompress

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharFileInfo::decompress — Розтискає поточний файл

### Опис

```methodsynopsis
public PharFileInfo::decompress(): bool
```

Цей метод розтискає файл усередині phar-архіву. Залежно від того, яким методом файл був стиснутий, потрібна наявність модулів [bzip2](ref.bzip2.html) або [zlib](ref.zlib.html). Так як ця функціональність змінює phar-архів, необхідно, щоб опція [phar.readonly](phar.configuration.html#ini.phar.readonly) було відключено, інакше внести зміни до архіву [Phar](class.phar.html) не вийде. На архіви [PharData](class.phardata.html) обмеження на запис не поширюється.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.html)якщо опція [phar.readonly](phar.configuration.html#ini.phar.readonly) включена, або відповідний модуль [bzip2](ref.bzip2.html)[zlib](ref.zlib.html) недоступний.

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::decompress()****

```php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    $file->compress(Phar::GZ);
    var_dump($file->isCompressed());
    $p['myfile.txt']->decompress();
    var_dump($file->isCompressed());
} catch (Exception $e) {
    echo 'Не удалось создать/изменить my.phar: ', $e;
}
?>
```

Результат виконання цього прикладу:

```
int(4096)
bool(false)
```

### Дивіться також

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.html) - Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.html) - Перевірити, чи стиснутий файл
-   [PharFileInfo::compress()](pharfileinfo.compress.html) - Стиснути поточний файл за допомогою zlib або bzip2
-   [Phar::canCompress()](phar.cancompress.html) - Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::isCompressed()](phar.iscompressed.html) - Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [Phar::compressFiles()](phar.compressfiles.html) - Стискає всі файли в поточному Phar-архіві
-   [Phar::decompressFiles()](phar.decompressfiles.html) - Розпаковує всі файли в поточному Phar-архіві
-   [Phar::compress()](phar.compress.html) - Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::decompress()](phar.decompress.html) - Розпаковує весь Phar-архів
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.html) - Повертає масив підтримуваних алгоритмів стиснення