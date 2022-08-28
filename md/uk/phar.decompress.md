Розпаковує весь Phar-архів

-   [« Phar::createDefaultStub](phar.createdefaultstub.html)
    
-   [Phar::decompressFiles »](phar.decompressfiles.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Розпаковує весь Phar-архів
    

# Phar::decompress

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::decompress — Розпаковує весь Phar-архів

### Опис

```methodsynopsis
public Phar::decompress(?string $extension = null): ?Phar
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.html) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.html)

Що стосується phar-архівами, заснованими на tar чи phar, цей метод розпаковує весь архів.

У випадку з phar-архівами, що базуються на zip, виклик даного методу зазнає невдачі і буде кинуто виняток. Для розпакування архіву, стиснутого за алгоритмом gzip, має бути включений модуль [zlib](ref.zlib.html); для розпакування архіву, стиснутого за алгоритмом bzip2, має бути включений модуль [bzip2](ref.bzip2.html). Як і у випадку з іншим функціоналом, що модифікує зміст phar-архіву, для успішної роботи даного методу необхідно, щоб INI-змінна [phar.readonly](phar.configuration.html#ini.phar.readonly) було відключено.

Крім того, цей метод автоматично змінює розширення файлу архіву: за замовчуванням `.phar` для phar-архівів та `.phar.tar` для phar-архівів, що базуються на tar. Як альтернатива розширення файлу може бути задано за допомогою другого параметра.

### Список параметрів

`extension`

Розширення розпакованого файлу за замовчуванням є `.phar` і `.phar.tar`. Цей параметр можна використовувати для завдання іншого розширення розпакованого файлу. Майте на увазі, що всі виконувані phar-архіви повинні містити `.phar` в імені файлу.

### Значення, що повертаються

Повертає об'єкт [Phar](class.phar.html) у разі успішного виконання та **`null`** у разі виникнення помилки.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.html), якщо INI-змінна [phar.readonly](phar.configuration.html#ini.phar.readonly) включена, модуль [zlib](ref.zlib.html) не доступний або модуль [bzip2](ref.bzip2.html) не увімкнуто.

### список змін

| Версия | Описание                                  |
|--------|-------------------------------------------|
|        | `extension` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **Phar::decompress()****

```php
<?php
$p = new Phar('/путь/к/my.phar', 0, 'my.phar.gz');
$p['myfile.txt'] = 'привет';
$p['myfile2.txt'] = 'привет';
$p3 = $p2->decompress(); // создаст /путь/к/my.phar
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
-   [Phar::compress()](phar.compress.html) - Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::getSupportedCompression()](phar.getsupportedcompression.html) - Повертає масив підтримуваних алгоритмів стиснення
-   [Phar::compressFiles()](phar.compressfiles.html) - Стискає всі файли у поточному Phar-архіві
-   [Phar::decompressFiles()](phar.decompressfiles.html) - Розпаковує всі файли в поточному Phar-архіві