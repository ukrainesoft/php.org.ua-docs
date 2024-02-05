---
navigation:
  - pharfileinfo.construct.md: '« PharFileInfo::\_\_construct'
  - pharfileinfo.delmetadata.md: 'PharFileInfo::delMetadata »'
  - index.md: PHP Manual
  - class.pharfileinfo.md: PharFileInfo
title: 'PharFileInfo::decompress'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharFileInfo::decompress

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharFileInfo::decompress — Розтискає поточний файл

### Опис

```methodsynopsis
public PharFileInfo::decompress(): bool
```

Цей метод розтискає файл усередині phar-архіву. Залежно від того, яким методом файл був стиснутий, потрібна наявність модулів [bzip2](ref.bzip2.md) або [zlib](ref.zlib.md). Так як ця функціональність змінює phar-архів, необхідно, щоб опція [phar.readonly](phar.configuration.md#ini.phar.readonly) було відключено, інакше внести зміни до архіву [Phar](class.phar.md) не вийде. На архіви [PharData](class.phardata.md) обмеження на запис не поширюється.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.md)якщо опція [phar.readonly](phar.configuration.md#ini.phar.readonly) включена, або відповідний модуль [bzip2](ref.bzip2.md) [zlib](ref.zlib.md)недоступен.

### Приклади

**Пример #1 Пример использования**PharFileInfo::decompress()\*\*\*\*

```php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    $file->compress(Phar::GZ);
    var_dump($file->isCompressed());
    $p['myfile.txt']->decompress();
    var_dump($file->isCompressed());
} catch (Exception $e) {
    echo 'Не удалось создать/изменить my.phar: ', $e;
}
?>
```

Результат виконання наведеного прикладу:

```
int(4096)
bool(false)
```

### Дивіться також

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.md) \- Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.md) \- Перевірити, чи стиснутий файл
-   [PharFileInfo::compress()](pharfileinfo.compress.md) \- Стиснути поточний файл за допомогою zlib або bzip2
-   [Phar::canCompress()](phar.cancompress.md) \- Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::isCompressed()](phar.iscompressed.md) \- Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [Phar::compressFiles()](phar.compressfiles.md) \- Стискає всі файли у поточному Phar-архіві
-   [Phar::decompressFiles()](phar.decompressfiles.md) \- Розпаковує всі файли в поточному Phar-архіві
-   [Phar::compress()](phar.compress.md) \- Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::decompress()](phar.decompress.md) \- Розпаковує весь Phar-архів
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.md) \- Повертає масив підтримуваних алгоритмів стиснення
