Перевірити, що phar-архів має заданий формат (tar/phar/zip)

-   [« Phar::isCompressed](phar.iscompressed.html)
    
-   [Phar::isValidPharFilename »](phar.isvalidpharfilename.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Перевірити, що phar-архів має заданий формат (tar/phar/zip)
    

# Phar::isFileFormat

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::isFileFormat — Перевірити, що phar-архів має заданий формат (tar/phar/zip)

### Опис

```methodsynopsis
public Phar::isFileFormat(int $format): bool
```

### Список параметрів

`format`

`Phar::PHAR` `Phar::TAR` або `Phar::ZIP`, залежно від формату, що перевіряється.

### Значення, що повертаються

Повертає **`true`**, якщо phar-архів має вказаний формат

### Помилки

У разі завдання некоректного формату викидається виняток [PharException](class.pharexception.html)

### Дивіться також

-   [Phar::convertToExecutable()](phar.converttoexecutable.html) - Конвертує phar-архів в інший формат файлу, що виконується.
-   [Phar::convertToData()](phar.converttodata.html) - Конвертує phar-архів в tar-або zip-файл, що не виконується.