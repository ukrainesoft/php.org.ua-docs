---
navigation:
  - phar.addfile.md: '« Phar::addFile'
  - phar.apiversion.md: 'Phar::apiVersion »'
  - index.md: PHP Manual
  - class.phar.md: Phar
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
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

За допомогою цього методу в phar-архів може бути доданий будь-який рядок. Файл буде збережено в архіві під ім'ям, вказаним у параметрі `localname`. Цей метод аналогічний [ZipArchive::addFromString()](ziparchive.addfromstring.md)

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
try {
    $a = new Phar('/путь/к/phar.phar');

    $a->addFromString('путь/к/file.txt', 'мой простой файл');
    $b = $a['путь/к/file.txt']->getContent();

    // для добавления содержимого из дескриптора потока для больших файлов используйте offsetSet()
    $c = fopen('/путь/к/hugefile.bin');
    $a['largefile.bin'] = $c;
    fclose($c);
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Примітки

> **Зауваження** [Phar::addFile()](phar.addfile.md) **Phar::addFromString()** і [Phar::offsetSet()](phar.offsetset.md) зберігає новий phar-архів щоразу при їхньому викликі. Якщо продуктивність викликає занепокоєння, натомість слід використовувати [Phar::buildFromDirectory()](phar.buildfromdirectory.md) або [Phar::buildFromIterator()](phar.buildfromiterator.md)

### Дивіться також

-   [Phar::offsetSet()](phar.offsetset.md) - Зміна вмісту файлу
-   [PharData::addFromString()](phardata.addfromstring.md) - Створити файл із заданим вмістом у tar/zip-архіві
-   [Phar::addFile()](phar.addfile.md) - Додає в phar-архів файл із файлової системи
-   [Phar::addEmptyDir()](phar.addemptydir.md) - Додає в phar-архів порожню директорію
