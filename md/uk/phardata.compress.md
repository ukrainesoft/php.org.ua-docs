Стискає весь архів tar/zip, використовуючи стиснення Gzip або Bzip2

-   [« PharData::buildFromIterator](phardata.buildfromiterator.html)
    
-   [PharData::compressFiles »](phardata.compressfiles.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Стискає весь архів tar/zip, використовуючи стиснення Gzip або Bzip2
    

# PharData::compress

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::compress — Стискає весь архів tar/zip, використовуючи стиснення Gzip або Bzip2

### Опис

```methodsynopsis
public PharData::compress(int $compression, ?string $extension = null): ?PharData
```

Для tar-архівів, цей метод здійснить стиснення всього архіву за допомогою gzip або bzip2. Результуючий файл можна розпакувати за допомогою команд gunzip або bunzip, або безпосередньо використовувати через модуль Phar.

Для zip-архівів цей метод викине виняток. Для gzip-стиснення повинен бути доступний модуль [zlib](ref.zlib.html). Для bzip2-стиснення повинен бути доступний модуль [bzip2](ref.bzip2.html)

Цей метод перейменовує архів, додаючи до його імені розширення `.gz` `.bz2` або навпаки, що прибирає його, якщо параметр типу стиснення заданий як `Phar::NONE`. Також можна явно вказати, яке розширення матиме файл.

### Список параметрів

`compression`

Одна з констант: `Phar::GZ` `Phar::BZ2`, або `Phar::NONE` для відключення компресії.

`extension`

За промовчанням файлу призначається розширення `.tar.gz` або `.tar.bz2` для стиснення та `.tar`, якщо стиснення вимкнено.

### Значення, що повертаються

Повертає об'єкт [PharData](class.phardata.html) у разі успішного виконання або **`null`** у разі виникнення помилки.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.html)якщо недоступний модуль [zlib](ref.zlib.html) або вимкнено модуль [bzip2](ref.bzip2.html)

### список змін

| Версия | Описание                                  |
|--------|-------------------------------------------|
|        | `extension` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **PharData::compress()****

```php
<?php
$p = new PharData('/path/to/my.tar');
$p['myfile.txt'] = 'hi';
$p['myfile2.txt'] = 'hi';
$p1 = $p->compress(Phar::GZ); // copies to /path/to/my.tar.gz
$p2 = $p->compress(Phar::BZ2); // copies to /path/to/my.tar.bz2
$p3 = $p2->compress(Phar::NONE); // exception: /path/to/my.tar already exists
?>
```

### Дивіться також

-   [Phar::compress()](phar.compress.html) - Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення