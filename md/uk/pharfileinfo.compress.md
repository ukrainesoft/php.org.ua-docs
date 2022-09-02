---
navigation:
  - pharfileinfo.chmod.md: '« PharFileInfo::chmod'
  - pharfileinfo.construct.md: 'PharFileInfo::construct »'
  - index.md: PHP Manual
  - class.pharfileinfo.md: PharFileInfo
title: 'PharFileInfo::compress'
---
# PharFileInfo::compress

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharFileInfo::compress — Стиснути поточний файл за допомогою zlib або bzip2

### Опис

```methodsynopsis
public PharFileInfo::compress(int $compression): bool
```

Цей метод стискає файл усередині phar-архіву за допомогою bzip2 чи zlib. Для конкретних алгоритмів стиснення необхідно, щоб були підключені модулі [bzip2](ref.bzip2.md) або [zlib](ref.zlib.md) відповідно. Також, якщо файл вже стиснутий, то для його розтискання буде потрібно відповідний модуль. Так як дана функціональність змінює вміст архіву, для його нормальної роботи необхідно, щоб INI-опція [phar.readonly](phar.configuration.md#ini.phar.readonly) було відключено, інакше не вдасться внести зміни до архіву [Phar](class.phar.md). Файли [PharData](class.phardata.md) не мають обмежень, пов'язаних із налаштуванням у php.ini.

### Список параметрів

`compression`

Стиснення має бути **`Phar::GZ`** або **`Phar::BZ2`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає [BadMethodCallException](class.badmethodcallexception.md), якщо INI-опція [phar.readonly](phar.configuration.md#ini.phar.readonly) увімкнено, або якщо відповідний модуль [bzip2](ref.bzip2.md)[zlib](ref.zlib.md) недоступний.

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::compress()****

```php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    var_dump($file->isCompressed(Phar::BZ2));
    $p['myfile.txt']->compress(Phar::BZ2);
    var_dump($file->isCompressed(Phar::BZ2));
} catch (Exception $e) {
    echo 'Операции создания/изменения на my.phar завершились ошибкой: ', $e;
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
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.md) - Перевірити, чи стиснутий файл
-   [PharFileInfo::decompress()](pharfileinfo.decompress.md) - Розтискає поточний файл
-   [Phar::canCompress()](phar.cancompress.md) - Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::isCompressed()](phar.iscompressed.md) - Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [Phar::compressFiles()](phar.compressfiles.md) - Стискає всі файли у поточному Phar-архіві
-   [Phar::decompressFiles()](phar.decompressfiles.md) - Розпаковує всі файли в поточному Phar-архіві
-   [Phar::compress()](phar.compress.md) - Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::decompress()](phar.decompress.md) - Розпаковує весь Phar-архів
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.md) - Повертає масив підтримуваних алгоритмів стиснення
