---
navigation:
  - phardata.addemptydir.md: '« PharData::addEmptyDir'
  - phardata.addfromstring.md: 'PharData::addFromString »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::addFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharData::addFile

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::addFile — Додати існуючі файли до tar/zip-архіву

### Опис

```methodsynopsis
public PharData::addFile(string $filename, ?string $localName = null): void
```

За допомогою цього методу можна додати до архіву будь-які файли чи URL-адреси. Якщо встановлено опціональний параметр `localname`, то файл буде додано до архіву із зазначеним ім'ям, інакше буде використано оригінальне ім'я з параметра `file`. Для URL локальне ім'я має бути вказано в обов'язковому порядку, інакше буде викинуто виняток. Метод аналогічний [ZipArchive::addFile()](ziparchive.addfile.md)

### Список параметрів

`filename`

Повний чи відносний шлях до файлу на диску.

`localName`

Шлях, яким файл необхідно додати в архів.

### Значення, що повертаються

Нічого не повертає, а у разі виникнення помилки викидає виняток.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `localName` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** PharData::addFile()\*\*\*\*

```php
<?php
try {
    $a = new PharData('/path/to/my.tar');

    $a->addFile('/full/path/to/file');
    // добавление файла
    $b = $a['full/path/to/file']->getContent();

    $a->addFile('/full/path/to/file', 'my/file.txt');
    $c = $a['my/file.txt']->getContent();

    // добавление URL
    $a->addFile('http://www.example.com', 'example.md');
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Примітки

> **Зауваження** **PharData::addFile()** [PharData::addFromString()](phardata.addfromstring.md)and[PharData::offsetSet()](phardata.offsetset.md)save a new phar archive each time they are called. If performance is a concern,[PharData::buildFromDirectory()](phardata.buildfromdirectory.md)or[PharData::buildFromIterator()](phardata.buildfromiterator.md)should be used instead.

### Дивіться також

-   [PharData::offsetSet()](phardata.offsetset.md) \- Зміна вмісту файлу
-   [Phar::addFile()](phar.addfile.md) \- Додає в phar-архів файл із файлової системи
-   [PharData::addFromString()](phardata.addfromstring.md) \- Додає файл з рядка до архіву tar/zip
-   [PharData::addEmptyDir()](phardata.addemptydir.md) \- Додати порожню директорію до tar/zip-архіву
