---
navigation:
  - phardata.copy.md: '« PharData::copy'
  - phardata.decompressfiles.md: 'PharData::decompressFiles »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::decompress'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharData::decompress

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::decompress — Розпакувати весь Phar-архів

### Опис

```methodsynopsis
public PharData::decompress(?string $extension = null): ?PharData
```

Для архівів типу tar цей метод розпаковує весь архів.

Для архівів типу Zip цей метод викине виняток. Для розтискання gzip-архівів має бути включений модуль [zlib](ref.zlib.md), а для bzip2, соответственно, модуль[bzip2](ref.bzip2.md)

Також цей метод автоматично змінює розширення файлу, за замовчуванням `.tar`. Розширення можна вказати явно за допомогою параметра `extension`

### Список параметрів

`extension`

По умолчанию при распаковке файлу меняется расширение на`.tar`. За допомогою цього параметра можна вказати нове розширення. Будьте обережні, тільки архіви, що запускаються, можуть містити `.phar` у своїх іменах.

### Значення, що повертаються

Повертає об'єкт типу [PharData](class.phardata.md) у разі успішного виконання та \*\*`null`\*\*в случае возникновения ошибки.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.md), якщо відсутній модуль, необхідний для розпакування: [zlib](ref.zlib.md) або [bzip2](ref.bzip2.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `extension` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**PharData::decompress()\*\*\*\*

```php
<?php
$p = new PharData('/path/to/my.tar.gz');
$p->decompress(); // creates /path/to/my.tar
?>
```

### Дивіться також

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.md) \- Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.md) \- Перевірити, чи стиснутий файл
-   [PharFileInfo::compress()](pharfileinfo.compress.md) \- Стиснути поточний файл за допомогою zlib або bzip2
-   [PharFileInfo::decompress()](pharfileinfo.decompress.md) \- Розтискає поточний файл
-   [PharData::compress()](phardata.compress.md) \- Стискає весь архів tar/zip, використовуючи стиснення Gzip або Bzip2
-   [Phar::canCompress()](phar.cancompress.md) \- Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::isCompressed()](phar.iscompressed.md) \- Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [PharData::compress()](phardata.compress.md) \- Стискає весь архів tar/zip, використовуючи стиснення Gzip або Bzip2
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.md) \- Повертає масив підтримуваних алгоритмів стиснення
-   [PharData::compressFiles()](phardata.compressfiles.md) \- Стиснути всі файли у поточному tar/zip-архіві
-   [PharData::decompressFiles()](phardata.decompressfiles.md) \- Розпакувати всі файли у поточному zip-архіві
