---
navigation:
  - phar.isbuffering.md: '« Phar::isBuffering'
  - phar.isfileformat.md: 'Phar::isFileFormat »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::isCompressed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::isCompressed

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::isCompressed — Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)

### Опис

```methodsynopsis
public Phar::isCompressed(): int|false
```

> **Зауваження** :
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly`в . В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі). Phar-архіви, засновані на zip, не можуть бути стиснуті цілком, тому цей метод завжди повертає \*\*`false`\*\*якщо він був викликаний на phar-архіві, заснованому на zip.

### Список параметрів

Немає параметрів.

### Значення, що повертаються

`Phar::GZ` `Phar::BZ2`или\*\*`false`\*\*

### Приклади

**Приклад #1 Приклад використання** Phar::isCompressed()\*\*\*\*

```php
<?php
try {
    $phar1 = new Phar('myphar.zip.phar');
    var_dump($phar1->isCompressed());
    $phar2 = new Phar('myuncompressed.tar.phar');
    var_dump($phar2->isCompressed());
    $phar2->compress(Phar::GZ);
    var_dump($phar2->isCompressed() == Phar::GZ);
} catch (Exception $e) {
}
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(false)
bool(true)
```

### Дивіться також

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.md) \- Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.md) \- Перевірити, чи стиснутий файл
-   [PharFileInfo::decompress()](pharfileinfo.decompress.md) \- Розтискає поточний файл
-   [PharFileInfo::compress()](pharfileinfo.compress.md) \- Стиснути поточний файл за допомогою zlib або bzip2
-   [Phar::decompress()](phar.decompress.md) \- Розпаковує весь Phar-архів
-   [Phar::compress()](phar.compress.md) \- Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::canCompress()](phar.cancompress.md) \- Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::compressFiles()](phar.compressfiles.md) \- Стискає всі файли у поточному Phar-архіві
-   [Phar::decompressFiles()](phar.decompressfiles.md) \- Розпаковує всі файли в поточному Phar-архіві
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.md) \- Повертає масив підтримуваних алгоритмів стиснення
