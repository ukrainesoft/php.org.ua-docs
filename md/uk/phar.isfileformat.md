---
navigation:
  - phar.iscompressed.md: '« Phar::isCompressed'
  - phar.isvalidpharfilename.md: 'Phar::isValidPharFilename »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::isFileFormat'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::isFileFormat

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::isFileFormat — Перевірити, що phar-архів має заданий формат (tar/phar/zip)

### Опис

```methodsynopsis
public Phar::isFileFormat(int $format): bool
```

### Список параметрів

`format`

`Phar::PHAR` `Phar::TAR`или`Phar::ZIP`, залежно від формату, що перевіряється.

### Значення, що повертаються

Повертає **`true`**, якщо phar-архів має вказаний формат

### Помилки

У разі завдання некоректного формату викидається виняток [PharException](class.pharexception.md)

### Дивіться також

-   [Phar::convertToExecutable()](phar.converttoexecutable.md) \- Конвертує phar-архів в інший формат файлу, що виконується.
-   [Phar::convertToData()](phar.converttodata.md) \- Конвертує phar-архів в tar-або zip-файл, що не виконується.
