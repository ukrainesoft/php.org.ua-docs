---
navigation:
  - phardata.buildfromiterator.md: '« PharData::buildFromIterator'
  - phardata.compressfiles.md: 'PharData::compressFiles »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::compress'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharData::compress

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::compress — Стискає весь архів tar/zip, використовуючи стиснення Gzip або Bzip2

### Опис

```methodsynopsis
public PharData::compress(int $compression, ?string $extension = null): ?PharData
```

Для tar-архівів, цей метод здійснить стиснення всього архіву за допомогою gzip або bzip2. Результуючий файл можна розпакувати за допомогою команд gunzip або bunzip, або безпосередньо використовувати через модуль Phar.

Для zip-архівів цей метод викине виняток. Для gzip-стиснення повинен бути доступний модуль [zlib](ref.zlib.md). Для bzip2-стиснення повинен бути доступний модуль [bzip2](ref.bzip2.md)

Цей метод перейменовує архів, додаючи до його імені розширення `.gz` `.bz2`или наоборот, убирающее его, если параметр типа сжатия задан как`Phar::NONE`. Також можна явно вказати, яке розширення матиме файл.

### Список параметрів

`compression`

Одна из констант:`Phar::GZ` `Phar::BZ2`, или`Phar::NONE` для відключення компресії.

`extension`

По умолчанию файлу назначится расширение`.tar.gz`или`.tar.bz2` для стиснення та `.tar`, якщо стиснення вимкнено.

### Значення, що повертаються

Повертає об'єкт [PharData](class.phardata.md) у разі успішного виконання або \*\*`null`\*\*в случае возникновения ошибки.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.md)якщо недоступний модуль [zlib](ref.zlib.md) або вимкнено модуль [bzip2](ref.bzip2.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `extension` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** PharData::compress()\*\*\*\*

```php
<?php
$p = new PharData('/path/to/my.tar');
$p['myfile.txt'] = 'hi';
$p['myfile2.txt'] = 'hi';
$p1 = $p->compress(Phar::GZ); // copies to /path/to/my.tar.gz
$p2 = $p->compress(Phar::BZ2); // copies to /path/to/my.tar.bz2
$p3 = $p2->compress(Phar::NONE); // exception: /path/to/my.tar already exists
?>
```

### Дивіться також

-   [Phar::compress()](phar.compress.md) \- Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
