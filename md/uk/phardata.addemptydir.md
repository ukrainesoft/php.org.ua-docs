---
navigation:
  - class.phardata.md: « PharData
  - phardata.addfile.md: 'PharData::addFile »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::addEmptyDir'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharData::addEmptyDir

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::addEmptyDir — Додати порожню директорію до tar/zip-архіву

### Опис

```methodsynopsis
public PharData::addEmptyDir(string $directory): void
```

За допомогою цього місця можна створити директорію шляхом `dirname`. Цей метод аналогічний [ZipArchive::addEmptyDir()](ziparchive.addemptydir.md)

### Список параметрів

`directory`

Шлях створюваної директорії

### Значення, що повертаються

Нічого не вертає. У разі помилок викидає виняток.

### Приклади

**Приклад #1 Приклад використання** PharData::addEmptyDir()\*\*\*\*

```php
<?php
try {
    $a = new PharData('/path/to/my.tar');

    $a->addEmptyDir('/full/path/to/file');
    // показывает, как хранится файл
    $b = $a['full/path/to/file']->isDir();
} catch (Exception $e) {
    // обрабатываем ошибки
}
?>
```

### Дивіться також

-   [Phar::addEmptyDir()](phar.addemptydir.md) \- Додає в phar-архів порожню директорію
-   [PharData::addFile()](phardata.addfile.md) \- Додати існуючі файли до tar/zip-архіву
-   [PharData::addFromString()](phardata.addfromstring.md) \- Додає файл з рядка до архіву tar/zip
