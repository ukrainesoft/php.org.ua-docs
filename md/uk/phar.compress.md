---
navigation:
  - phar.canwrite.md: '« Phar::canWrite'
  - phar.compressfiles.md: 'Phar::compressFiles »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::compress'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::compress

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::compress — Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення

### Опис

```methodsynopsis
public Phar::compress(int $compression, ?string $extension = null): ?Phar
```

> **Зауваження** :
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly`в . В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

У разі використання з phar-архівами, заснованими на tar або phar, цей метод стискає весь архів, використовуючи gzip- або bzip2-стиск. Отриманий файл може бути оброблений однією з команд gunzip/bunzip; до нього можна отримати прямий доступ, використовуючи модуль Phar.

У разі використання з phar-архівами, що базуються на zip, виклик цього методу зазнає невдачі і буде кинуто виняток. Для стиснення за алгоритмом gzip має бути включений модуль [zlib](ref.zlib.md). Для стиснення алгоритму bzip2 повинен бути включений модуль [bzip2](ref.bzip2.md). Як і у випадку з іншим функціоналом, що модифікує зміст phar-архіву, для успішної роботи даного методу необхідно, щоб INI-змінна [phar.readonly](phar.configuration.md#ini.phar.readonly) було відключено.

Крім того, цей метод автоматично перейменовує архів, додаючи `.gz` `.bz2` або видаляючи розширення, якщо перший параметр був переданий `Phar::NONE`, що повідомляє про необхідність розпакування. Як альтернатива розширення файлу може бути задано за допомогою другого параметра.

### Список параметрів

`compression`

Стиснення має бути визначено однією з констант: `Phar::GZ` `Phar::BZ2`для использования соответствующего алгоритма сжатия, или`Phar::NONE` для розпакування.

`extension`

Для сжатия phar-архивов по умолчанию используется расширение`.phar.gz`или`.phar.bz2`, а для сжатия tar-архивов —`.phar.tar.gz`или`.phar.tar.bz2`. У разі розпакування, розширеннями за замовчуванням є `.phar`и`.phar.tar`

### Значення, що повертаються

Повертає об'єкт [Phar](class.phar.md)или\*\*`null`\*\*в случае возникновения ошибки.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.md), если INI-переменная[phar.readonly](phar.configuration.md#ini.phar.readonly)включена, модуль[zlib](ref.zlib.md) не доступний або модуль [bzip2](ref.bzip2.md) не увімкнуто.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `extension` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** Phar::compress()\*\*\*\*

```php
<?php
$p = new Phar('/путь/к/my.phar', 0, 'my.phar');
$p['myfile.txt'] = 'привет';
$p['myfile2.txt'] = 'привет';
$p1 = $p->compress(Phar::GZ); // копирует в /путь/к/my.phar.gz
$p2 = $p->compress(Phar::BZ2); // копирует в /путь/к/my.phar.bz2
$p3 = $p2->compress(Phar::NONE); // исключение: /путь/к/my.phar уже существует
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
-   [Phar::decompress()](phar.decompress.md) \- Розпаковує весь Phar-архів
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.md) \- Повертає масив підтримуваних алгоритмів стиснення
-   [Phar::compressFiles()](phar.compressfiles.md) \- Стискає всі файли у поточному Phar-архіві
-   [Phar::decompressFiles()](phar.decompressfiles.md) \- Розпаковує всі файли в поточному Phar-архіві
