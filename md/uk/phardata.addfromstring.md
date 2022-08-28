Створити файл із заданим вмістом у tar/zip-архіві

-   [« PharData::addFile](phardata.addfile.html)
    
-   [PharData::buildFromDirectory »](phardata.buildfromdirectory.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Створити файл із заданим вмістом у tar/zip-архіві
    

# PharData::addFromString

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::addFromString — Створити файл із заданим вмістом у tar/zip-архіві

### Опис

```methodsynopsis
public PharData::addFromString(string $localName, string $contents): void
```

Цей метод дозволяє створити всередині архіву файл із заданим текстом. Файл буде збережено на шляху `localname`. Цей метод аналогічний [ZipArchive::addFromString()](ziparchive.addfromstring.html)

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
try {
    $a = new PharData('/path/to/my.tar');

    $a->addFromString('path/to/file.txt', 'my simple file');
    $b = $a['path/to/file.txt']->getContent();

    // Для добавления содержимого через потоковую обёртку для больших файлов, используйте offsetSet()
    $c = fopen('/path/to/hugefile.bin');
    $a['largefile.bin'] = $c;
    fclose($c);
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Примітки

> **Зауваження** [PharData::addFile()](phardata.addfile.html) **PharData::addFromString()** and [PharData::offsetSet()](phardata.offsetset.html) Залишити новий ріг архіву кожен час вони називаються. If performance is a concern, [PharData::buildFromDirectory()](phardata.buildfromdirectory.html) ор [PharData::buildFromIterator()](phardata.buildfromiterator.html) should be used instead.

### Дивіться також

-   [PharData::offsetSet()](phardata.offsetset.html) - Зміна вмісту файлу
-   [Phar::addFromString()](phar.addfromstring.html) - Додає в phar-архів файл із рядка
-   [PharData::addFile()](phardata.addfile.html) - Додати існуючі файли до tar/zip-архіву
-   [PharData::addEmptyDir()](phardata.addemptydir.html) - Додати порожню директорію до tar/zip-архіву