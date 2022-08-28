Розпаковує всі файли в поточному Phar-архіві

-   [« Phar::decompress](phar.decompress.html)
    
-   [Phar::delMetadata »](phar.delmetadata.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Розпаковує всі файли в поточному Phar-архіві
    

# Phar::decompressFiles

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::decompressFiles — Розпаковує всі файли в поточному Phar-архіві

### Опис

```methodsynopsis
public Phar::decompressFiles(): bool
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.html) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.html)

У разі використання з phar-архівами, заснованими на tar, цей метод викидає виняток [BadMethodCallException](class.badmethodcallexception.html), оскільки стиснення окремих файлів усередині tar-архіву не підтримується цим форматом. Для стиснення цілого phar-архіву, заснованого на tar, використовуйте [Phar::compress()](phar.compress.html)

У разі використання з phar-архівами, що базуються на zip або phar, цей метод розпаковує всі файли в Phar-архіві. Якщо будь-які файли всередині архіву були стиснуті за допомогою bzip2/zlib-стиснення, то для можливості скористатися даним методом повинен бути включений модуль [zlib](ref.zlib.html) або [bzip2](ref.bzip2.html). Як і у випадку з іншим функціоналом, що модифікує зміст phar-архіву, для успішної роботи даного методу необхідно, щоб INI-змінна [phar.readonly](phar.configuration.html#ini.phar.readonly) було відключено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.html), якщо INI-змінна [phar.readonly](phar.configuration.html#ini.phar.readonly) включена, модуль [zlib](ref.zlib.html) недоступний або якщо будь-які файли всередині архіву були стиснуті з використанням bzip2-стиснення та модуль [bzip2](ref.bzip2.html) не увімкнуто.

### Приклади

**Приклад #1 Приклад використання **Phar::decompressFiles()****

```php
<?php
$p = new Phar('/путь/к/my.phar', 0, 'my.phar');
$p['myfile.txt'] = 'привет';
$p['myfile2.txt'] = 'привет';
$p->compressFiles(Phar::GZ);
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
$p->decompressFiles();
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

-   [PharFileInfo::getCompressedSize()](pharfileinfo.getcompressedsize.html) - Отримати реальний розмір файлу на диску з урахуванням стиснення
-   [PharFileInfo::isCompressed()](pharfileinfo.iscompressed.html) - Перевірити, чи стиснутий файл
-   [PharFileInfo::compress()](pharfileinfo.compress.html) - Стиснути поточний файл за допомогою zlib або bzip2
-   [PharFileInfo::decompress()](pharfileinfo.decompress.html) - Розтискає поточний файл
-   [Phar::canCompress()](phar.cancompress.html) - Перевіряє, чи підтримує модуль phar стиск з використанням zlib або bzip2
-   [Phar::isCompressed()](phar.iscompressed.html) - Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [Phar::compressFiles()](phar.compressfiles.html) - Стискає всі файли в поточному Phar-архіві
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.html) - Повертає масив підтримуваних алгоритмів стиснення
-   [Phar::compress()](phar.compress.html) - Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::decompress()](phar.decompress.html) - Розпаковує весь Phar-архів