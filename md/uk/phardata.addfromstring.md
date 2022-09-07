---
navigation:
  - phardata.addfile.md: '« PharData::addFile'
  - phardata.buildfromdirectory.md: 'PharData::buildFromDirectory »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::addFromString'
---
# PharData::addFromString

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::addFromString — Створити файл із заданим вмістом у tar/zip-архіві

### Опис

```methodsynopsis
public PharData::addFromString(string $localName, string $contents): void
```

Цей метод дозволяє створити всередині архіву файл із заданим текстом. Файл буде збережено на шляху `localname`. Цей метод аналогічний [ZipArchive::addFromString()](ziparchive.addfromstring.md)

### Список параметрів

`localName`

Шлях створюваного файлу.

`contents`

Вміст файлу у вигляді рядка

### Значення, що повертаються

Нічого не повертає, у разі помилки викидає виняток.

### Приклади

**Приклад #1 Приклад використання **PharData::addFromString()****

```php
<?php
try {
    $a = new PharData('/path/to/my.tar');

    $a->addFromString('path/to/file.txt', 'my simple file');
    $b = $a['path/to/file.txt']->getContent();

    // Для добавления содержимого через потоковую обёртку для больших файлов, используйте offsetSet()
    $c = fopen('/path/to/hugefile.bin');
    $a['largefile.bin'] = $c;
    fclose($c);
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Примітки

> **Зауваження** [PharData::addFile()](phardata.addfile.md) **PharData::addFromString()** and [PharData::offsetSet()](phardata.offsetset.md) Залишити новий ріг архіву кожен час вони називаються. If performance is a concern, [PharData::buildFromDirectory()](phardata.buildfromdirectory.md) ор [PharData::buildFromIterator()](phardata.buildfromiterator.md) should be used instead.

### Дивіться також

-   [PharData::offsetSet()](phardata.offsetset.md) - Зміна вмісту файлу
-   [Phar::addFromString()](phar.addfromstring.md) - Додає в phar-архів файл із рядка
-   [PharData::addFile()](phardata.addfile.md) - Додати існуючі файли до tar/zip-архіву
-   [PharData::addEmptyDir()](phardata.addemptydir.md) - Додати порожню директорію до tar/zip-архіву
