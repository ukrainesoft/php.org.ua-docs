Додати порожню директорію до tar/zip-архіву

-   [« PharData](class.phardata.html)
    
-   [PharData::addFile »](phardata.addfile.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Додати порожню директорію до tar/zip-архіву
    

# PharData::addEmptyDir

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::addEmptyDir — Додати порожню директорію до tar/zip-архіву

### Опис

```methodsynopsis
public PharData::addEmptyDir(string $directory): void
```

За допомогою цього місця можна створити директорію шляхом `dirname`. Цей метод аналогічний [ZipArchive::addEmptyDir()](ziparchive.addemptydir.html)

### Список параметрів

`directory`

Шлях створюваної директорії

### Значення, що повертаються

Нічого не вертає. У разі помилок викидає виняток.

### Приклади

**Приклад #1 Приклад використання **PharData::addEmptyDir()****

```php
<?php
try {
    $a = new PharData('/path/to/my.tar');

    $a->addEmptyDir('/full/path/to/file');
    // показывает, как хранится файл
    $b = $a['full/path/to/file']->isDir();
} catch (Exception $e) {
    // обрабатываем ошибки
}
?>
```

### Дивіться також

-   [Phar::addEmptyDir()](phar.addemptydir.html) - Додає в phar-архів порожню директорію
-   [PharData::addFile()](phardata.addfile.html) - Додати існуючі файли до tar/zip-архіву
-   [PharData::addFromString()](phardata.addfromstring.html) - Створити файл із заданим вмістом у tar/zip-архіві