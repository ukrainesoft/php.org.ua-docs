---
navigation:
  - phar.decompress.md: '« Phar::decompress'
  - phar.delmetadata.md: 'Phar::delMetadata »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::decompressFiles'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::decompressFiles

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::decompressFiles — Розпаковує всі файли в поточному Phar-архіві

### Опис

```methodsynopsis
public Phar::decompressFiles(): bool
```

> **Зауваження** :
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly`в . В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

У разі використання з phar-архівами, заснованими на tar, цей метод викидає виняток [BadMethodCallException](class.badmethodcallexception.md), оскільки стиснення окремих файлів усередині tar-архіву не підтримується цим форматом. Для стиснення цілого phar-архіву, заснованого на tar, використовуйте [Phar::compress()](phar.compress.md)

У разі використання з phar-архівами, що базуються на zip або phar, цей метод розпаковує всі файли в Phar-архіві. Якщо будь-які файли всередині архіву були стиснуті за допомогою bzip2/zlib-стиснення, то для можливості скористатися даним методом повинен бути включений модуль [zlib](ref.zlib.md) або [bzip2](ref.bzip2.md). Як і у випадку з іншим функціоналом, що модифікує зміст phar-архіву, для успішної роботи даного методу необхідно, щоб INI-змінна [phar.readonly](phar.configuration.md#ini.phar.readonly) було відключено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.md), если INI-переменная[phar.readonly](phar.configuration.md#ini.phar.readonly)включена, модуль[zlib](ref.zlib.md) недоступний або якщо будь-які файли всередині архіву були стиснуті з використанням bzip2-стиснення та модуль [bzip2](ref.bzip2.md) не увімкнуто.

### Приклади

**Приклад #1 Приклад використання** Phar::decompressFiles()\*\*\*\*

```php
<?php
$p = new Phar('/путь/к/my.phar', 0, 'my.phar');
$p['myfile.txt'] = 'привет';
$p['myfile2.txt'] = 'привет';
$p->compressFiles(Phar::GZ);
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
$p->decompressFiles();
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
?>
```

Результат виконання наведеного прикладу:

```
string(10) "myfile.txt"
int(4096)
bool(false)
bool(true)
string(11) "myfile2.txt"
int(4096)
bool(false)
bool(true)
string(10) "myfile.txt"
bool(false)
bool(false)
bool(false)
string(11) "myfile2.txt"
bool(false)
bool(false)
bool(false)
```

### Дивіться також

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.md) \- Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.md) \- Перевірити, чи стиснутий файл
-   [PharFileInfo::compress()](pharfileinfo.compress.md) \- Стиснути поточний файл за допомогою zlib або bzip2
-   [PharFileInfo::decompress()](pharfileinfo.decompress.md) \- Розтискає поточний файл
-   [Phar::canCompress()](phar.cancompress.md) \- Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::isCompressed()](phar.iscompressed.md) \- Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [Phar::compressFiles()](phar.compressfiles.md) \- Стискає всі файли у поточному Phar-архіві
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.md) \- Повертає масив підтримуваних алгоритмів стиснення
-   [Phar::compress()](phar.compress.md) \- Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::decompress()](phar.decompress.md) \- Розпаковує весь Phar-архів
