Розпакувати весь Phar-архів

-   [« PharData::copy](phardata.copy.html)
    
-   [PharData::decompressFiles »](phardata.decompressfiles.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Розпакувати весь Phar-архів
    

# PharData::decompress

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::decompress — Розпакувати весь Phar-архів

### Опис

```methodsynopsis
public PharData::decompress(?string $extension = null): ?PharData
```

Для архівів типу tar цей метод розпаковує весь архів.

Для архівів типу Zip цей метод викине виняток. Для розтискання gzip-архівів має бути включений модуль [zlib](ref.zlib.html), а для bzip2, відповідно, модуль [bzip2](ref.bzip2.html)

Також цей метод автоматично змінює розширення файлу, за замовчуванням `.tar`. Розширення можна вказати явно за допомогою параметра `extension`

### Список параметрів

`extension`

За замовчуванням під час розпакування файлу змінюється розширення на `.tar`. За допомогою цього параметра можна вказати нове розширення. Будьте обережні, тільки архіви, що запускаються, можуть містити `.phar` у своїх іменах.

### Значення, що повертаються

Повертає об'єкт типу [PharData](class.phardata.html) у разі успішного виконання та **`null`** у разі виникнення помилки.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.html), якщо відсутній модуль, необхідний для розпакування: [zlib](ref.zlib.html) або [bzip2](ref.bzip2.html)

### список змін

| Версия | Описание                                  |
|--------|-------------------------------------------|
|        | `extension` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **PharData::decompress()****

```php
<?php
$p = new PharData('/path/to/my.tar.gz');
$p->decompress(); // creates /path/to/my.tar
?>
```

### Дивіться також

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.html) - Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.html) - Перевірити, чи стиснутий файл
-   [PharFileInfo::compress()](pharfileinfo.compress.html) - Стиснути поточний файл за допомогою zlib або bzip2
-   [PharFileInfo::decompress()](pharfileinfo.decompress.html) - Розтискає поточний файл
-   [PharData::compress()](phardata.compress.html) - Стискає весь архів tar/zip, використовуючи стиснення Gzip або Bzip2
-   [Phar::canCompress()](phar.cancompress.html) - Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::isCompressed()](phar.iscompressed.html) - Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [PharData::compress()](phardata.compress.html) - Стискає весь архів tar/zip, використовуючи стиснення Gzip або Bzip2
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.html) - Повертає масив підтримуваних алгоритмів стиснення
-   [PharData::compressFiles()](phardata.compressfiles.html) - Стиснути всі файли у поточному tar/zip-архіві
-   [PharData::decompressFiles()](phardata.decompressfiles.html) - Розпакувати всі файли у поточному zip-архіві