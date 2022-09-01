---
navigation:
  - phar.addfile.html: '« Phar::addFile'
  - phar.apiversion.html: 'Phar::apiVersion »'
  - index.html: PHP Manual
  - class.phar.html: Phar
title: 'Phar::addFromString'
---
# Phar::addFromString

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::addFromString — Додає в phar-архів файл з рядка

### Опис

```methodsynopsis
public Phar::addFromString(string $localName, string $contents): void
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.html) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.html)

За допомогою цього методу в phar-архів може бути доданий будь-який рядок. Файл буде збережено в архіві під ім'ям, вказаним у параметрі `localname`. Цей метод аналогічний [ZipArchive::addFromString()](ziparchive.addfromstring.html)

### Список параметрів

`localName`

Шлях, яким файл буде збережено в архіві.

`contents`

Вміст файлу для збереження.

### Значення, що повертаються

Немає значення, що повертається, у разі виникнення помилки викидається виняток.

### Приклади

**Приклад #1 Приклад використання **Phar::addFromString()****

```php
<?php
try {
    $a = new Phar('/путь/к/phar.phar');

    $a->addFromString('путь/к/file.txt', 'мой простой файл');
    $b = $a['путь/к/file.txt']->getContent();

    // для добавления содержимого из дескриптора потока для больших файлов используйте offsetSet()
    $c = fopen('/путь/к/hugefile.bin');
    $a['largefile.bin'] = $c;
    fclose($c);
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Примітки

> **Зауваження** [Phar::addFile()](phar.addfile.html) **Phar::addFromString()** і [Phar::offsetSet()](phar.offsetset.html) зберігає новий phar-архів щоразу при їхньому викликі. Якщо продуктивність викликає занепокоєння, натомість слід використовувати [Phar::buildFromDirectory()](phar.buildfromdirectory.html) або [Phar::buildFromIterator()](phar.buildfromiterator.html)

### Дивіться також

-   [Phar::offsetSet()](phar.offsetset.html) - Зміна вмісту файлу
-   [PharData::addFromString()](phardata.addfromstring.html) - Створити файл із заданим вмістом у tar/zip-архіві
-   [Phar::addFile()](phar.addfile.html) - Додає в phar-архів файл із файлової системи
-   [Phar::addEmptyDir()](phar.addemptydir.html) - Додає в phar-архів порожню директорію
